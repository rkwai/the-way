# Service API Module

Use this directory to implement the capabilities listed in the Money & Data PRD (`agent-artifacts/product/prd-data-flow.md`).

## Quick Commands
| Command | Purpose |
|---------|---------|
| `npm install` | Install dependencies |
| `npm run dev` | Start local dev server |
| `npm run build` | Compile for production |
| `npm test` | Run service tests |

## Implementation Notes
- Keep endpoints aligned with the “Release Scope” table in the PRD.
- Update migrations or infrastructure scripts under `/migrations` and reference them in the Product log.
- Instrument requests using the metrics defined in the Market & Business Analysis.

## Deployment
- Staging: `npm run deploy:staging`
- Production: `npm run deploy:prod`

Document any changes back in `agent-artifacts/product/prd-data-flow.md` and `agents/changelog/prd-data-flow.md`.
