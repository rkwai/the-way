# Agent Tasks

Reusable task templates that Codex agents execute. Each YAML file documents:
- `objective` and context.
- Required inputs (artifacts or data sources).
- Ordered steps that Codex or a teammate should follow.
- `evidence` that must be produced (usually updates in `agent-artifacts/` and `changelog/`).

Agents reference these task files in their `workflows` sections.
