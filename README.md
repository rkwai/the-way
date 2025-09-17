# Codex Product Workspace

This template keeps product development focused on three artifacts that move market share and revenue. The economy → market → company money flow feeds the internal data flow, which in turn powers the user journeys:
1. **Money Flow** – Data Engineer (business mindset)
2. **Data Flow** – Backend Engineer (product mindset)
3. **User Flow** – Frontend Engineer (designer mindset)

## How to Use
1. Install and authenticate the Codex CLI.
2. Clone this repo and adjust names to your organisation.
3. For each agent (`agents/*.yaml`), execute the listed workflows by running the referenced tasks in order (e.g. `codex run agents/tasks/analysis-market-scan.yaml`).
4. After each task, update the relevant doc in `artifacts/` and append evidence to the matching log under `agents/logs/`.
5. Only mark a cycle complete when the artifact and log both reflect the latest work.

## Repository Map
```
.
├── workspace.yaml         # Registers agents for Codex
├── agents/
│   ├── data.yaml           # Data engineer definition
│   ├── backend.yaml        # Backend engineer definition
│   ├── frontend.yaml       # Frontend engineer definition
│   ├── tasks/              # Task scripts used by each agent
│   ├── tools/              # Tool references (market, analytics, design, API)
│   └── logs/               # Evidence captured after each workflow run
├── artifacts/
│   ├── analysis/market-business-flow.md   # Market & business analysis
│   ├── product/prd-data-flow.md           # Money & data-focused PRD
│   └── ux/user-flow-map.md               # Experience blueprint
├── environment-profiles/   # Local, staging, and production profiles
└── products/               # Example codebases to implement capabilities
```

## Agent Workflows
Refer to each agent YAML for the ordered tasks:
- Data Engineer → `analysis` (analysis-market-scan, analysis-money-flow, analysis-implementation)
- Backend Engineer → `product-blueprint` (product-prd-draft, product-data-flow, product-implement-backend)
- Frontend Engineer → `experience` (ux-user-flows, ux-components, ux-implement-frontend)

## Why These Three Artifacts
| Artifact | Owner | What | Why | Evidence |
|----------|-------|------|-----|----------|
| Market & Business Analysis | Data Engineer | Economy → market → company money flow diagram, market sizing, demand signals, instrumentation plan | Proves there is revenue to capture and defines how we measure it | `artifacts/analysis/market-business-flow.md` + `agents/logs/market-business-flow.md` |
| Money & Data PRD | Backend Engineer | Opportunity narrative, data flow across company products/services, API capability scope | Aligns engineering work with revenue paths and data obligations | `artifacts/product/prd-data-flow.md` + `agents/logs/prd-data-flow.md` |
| Experience Blueprint | Frontend Engineer | Entry URLs, user flow diagrams, component/state map, launch handoff notes | Ensures customers can reach and experience the value we monetise | `artifacts/ux/user-flow-map.md` + `agents/logs/user-flow-map.md` |

Stay lightweight: keep docs current, link supporting tools, and record every workflow run in the logs.
