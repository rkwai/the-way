# Codex Product Workspace

This template keeps product development focused on three artifacts that move market share and revenue. The economy → market → company money flow feeds the internal data flow, which in turn powers the user journeys:
1. **Money Flow** – Data Engineer (business mindset)
2. **Data Flow** – Backend Engineer (product mindset)
3. **User Flow** – Frontend Engineer (designer mindset)

## How to Use
1. Install and authenticate the Codex CLI.
2. Clone this repo, adjust names to your organisation, and fill in any required context (e.g. `agent-data-sources/`).
3. From the repository root, start a Codex session so it loads `workspace.yaml` (for example, run `codex --cd /path/to/the-way`).
4. Launch the agent you need (`data`, `backend`, or `frontend`) from inside the CLI; Codex will step through the workflows declared in `agents/<agent>.yaml`.
5. Let each agent drive the creation or refresh of the linked artifacts and logs. Review the updates, make any company-specific edits, and commit when the documentation and changelog entries reflect the latest cycle.

## Repository Map
```
.
├── workspace.yaml         # Registers agents for Codex
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
├── changelog/            # Log templates for money/data/user flows + architecture/observability
├── agent-data-sources/    # Templates for external data (market, analytics, design, API)
├── environment-profiles/   # Local, staging, and production profiles
└── products/               # Example codebases to implement capabilities
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
