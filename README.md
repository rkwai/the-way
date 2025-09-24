# Codex Product Workspace

This template keeps product development focused on three artifacts that move market share and revenue. The economy → market → company money flow feeds the internal data flow, which in turn powers the user journeys:
1. **Money Flow** – Data Engineer (business mindset)
2. **Data Flow** – Backend Engineer (product mindset)
3. **User Flow** – Frontend Engineer (designer mindset)

## How to Use
1. Copy the contents of this repository into the scaffolding folder of your product workspace or mono-repo.
2. Install and authenticate the Codex CLI.
3. Tailor names and conventions across `agents/`, `agent-artifacts/`, and `changelog/` to match your organisation.
4. Wire these agents into your Codex workspace configuration (e.g., add them to your existing `workspace.yaml` so the `data`, `backend`, and `frontend` agents reference the YAML files in `agents/`).
5. Encourage your team to populate every template in `agent-data-sources/` before touching the agents so the external context is fresh.
6. Verify the accuracy and completeness of those data-source files (fix gaps, add citations, confirm owners).
7. From the repository root, start a Codex session with the workspace configuration you just wired up (for example, run `codex --cd /path/to/the-way`) and ask Codex to execute the agents in order: `data`, then `backend`, then `frontend`.
8. Let the agents fill out the linked artifacts and changelog entries, review the generated documentation, and commit once everything reflects the validated sources.

## Repository Map
```
.
├── agents/
│   ├── data.yaml           # Data engineer definition
│   ├── backend.yaml        # Backend engineer definition
│   ├── frontend.yaml       # Frontend engineer definition
│   └── tasks/              # Task scripts used by each agent
├── agent-artifacts/
│   ├── analysis/market-opportunity.md     # Market opportunity summary
│   ├── analysis/market-business-flow.md   # Money flow diagram
│   ├── product/prd-data-flow.md           # Money & data-focused PRD
│   ├── ux/user-flow-map.md                # Experience blueprint
│   ├── architecture/system-map.md         # System topology & decisions
│   └── observability/plan.md              # Product + technical signals
├── agent-data-sources/    # Templates for external data (market, analytics, design, API)
├── changelog/             # Log templates for money/data/user flows + architecture/observability
└── README.md
```

## Agent Workflows
Refer to each agent YAML for the agent purpose and ordered tasks:
- Data Engineer → `analysis` (analysis-market-demand, analysis-money-flow, analysis-implementation)
- Backend Engineer → `product-blueprint` (product-prd-draft, product-data-flow, product-implement-backend)
- Frontend Engineer → `experience` (ux-user-flows, ux-components, ux-implement-frontend)

## Why These Three Artifacts
| Artifact | Owner | What | Why | Evidence |
|----------|-------|------|-----|----------|
| Market-Business-Flow | Data Engineer | Money-flow map plus quantified demand signals and instrumentation checkpoints. | Confirms there is existing demand and shows how money moves from the economy into the company. | `agent-artifacts/analysis/market-business-flow.md`, `changelog/market-business-flow.md` |
| PRD-Data-Flow | Backend Engineer | PRD that ties monetisation to container/service data flows, API scope, and architecture + observability updates. | Aligns implementation work with revenue-critical data movement and keeps the system map cohesive. | `agent-artifacts/product/prd-data-flow.md`, `changelog/prd-data-flow.md` |
| User-Flow-Map | Frontend Engineer | User-flow blueprint covering entry points, UI states, and supporting services with a data-flow summary. | Ensures customers reach monetised capabilities and that UX changes stay in sync with backend/data plans. | `agent-artifacts/ux/user-flow-map.md`, `changelog/user-flow-map.md` |


Maintaining `agent-artifacts/architecture/system-map.md` keeps the technical topology coherent as money and data flows evolve. Logging updates in `changelog/architecture.md` makes those decisions auditable and shareable across teams. The observability pair (`agent-artifacts/observability/plan.md` + `changelog/observability.md`) ensures we prove value end-to-end—tracking the business metrics that matter and the technical signals that guarantee customers feel the impact.

`agent-data-sources/` contains blank templates for the external inputs you rely on (market reports, analytics portals, design repositories). Fill them in with links or instructions so agents and humans know where to pull context.

Stay lightweight: keep docs current, document external sources, and record every workflow run in the logs.
