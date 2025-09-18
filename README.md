# Codex Product Workspace

This template keeps product development focused on three artifacts that move market share and revenue. The economy → market → company money flow feeds the internal data flow, which in turn powers the user journeys:
1. **Money Flow** – Data Engineer (business mindset)
2. **Data Flow** – Backend Engineer (product mindset)
3. **User Flow** – Frontend Engineer (designer mindset)

## How to Use
1. Install and authenticate the Codex CLI.
2. Clone this repo and adjust names to your organisation.
3. For each agent (`agents/*.yaml`), execute the listed workflows by running the referenced tasks in order (e.g. `codex run agents/tasks/analysis-market-demand.yaml`).
4. After each task, update the relevant doc in `agent-artifacts/` and append evidence to the matching log under `changelog/`.
5. Only mark a cycle complete when the artifact and log both reflect the latest work.

## Repository Map
```
.
├── workspace.yaml         # Registers agents for Codex
├── agents/
│   ├── data.yaml           # Data engineer definition
│   ├── backend.yaml        # Backend engineer definition
│   └── frontend.yaml       # Frontend engineer definition
├── agents/tasks/           # Task scripts used by each agent
├── agent-artifacts/
│   ├── analysis/market-opportunity.md     # Market opportunity summary
│   ├── analysis/market-business-flow.md   # Money flow diagram
│   ├── product/prd-data-flow.md           # Money & data-focused PRD
│   ├── ux/user-flow-map.md                # Experience blueprint
│   ├── architecture/system-map.md         # System topology & decisions
│   └── observability/plan.md              # Product + technical signals
├── changelog/            # Log templates for money/data/user flows + architecture/observability
├── agent-data-sources/ # External data sources (market, analytics, design, API)
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
| Market & Business Analysis | Data Engineer | Market opportunity analysis, demand signals, money flow diagram, instrumentation plan | Proves there is revenue to capture and defines how we measure it | `agent-artifacts/analysis/market-opportunity.md`, `agent-artifacts/analysis/market-business-flow.md`, `changelog/market-opportunity.md`, `changelog/market-business-flow.md` |
| Money & Data PRD | Backend Engineer | Opportunity narrative, data flow across company products/services, API capability scope | Aligns engineering work with revenue paths and data obligations | `agent-artifacts/product/prd-data-flow.md` + `changelog/prd-data-flow.md` |
| Experience Blueprint | Frontend Engineer | Entry URLs, user flow diagrams, component/state map, launch handoff notes | Ensures customers can reach and experience the value we monetise | `agent-artifacts/ux/user-flow-map.md` + `changelog/user-flow-map.md` |


Maintaining `agent-artifacts/architecture/system-map.md` keeps the technical topology coherent as money and data flows evolve. Logging updates in `changelog/architecture.md` makes those decisions auditable and shareable across teams. The observability pair (`agent-artifacts/observability/plan.md` + `changelog/observability.md`) ensures we prove value end-to-end—tracking the business metrics that matter and the technical signals that guarantee customers feel the impact.

`agent-data-sources/` contains blank templates for the external inputs you rely on (market reports, analytics portals, design repositories). Fill them in with links or instructions so agents and humans know where to pull context.

Stay lightweight: keep docs current, document external sources, and record every workflow run in the logs.
