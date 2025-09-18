# Product Requirements Document (Money & Data Focus)

## Opportunity
- Customer problem:
- Business impact:
- Success metric:

## Money Flow Summary
- Revenue sources:
- Cost structure:
- Guardrails / compliance:

## Data Flow Diagram (C3 Mermaid)
```mermaid
flowchart LR
    subgraph Container_A
        ServiceA[Service A]
        ServiceB[Service B]
    end
    subgraph Container_B
        ServiceC[Service C]
    end
    ServiceA -->|Event| ServiceC
    ServiceB -->|API| ServiceC
    ServiceC --> DataStore[(Data Store)]
```
- API capabilities (name, purpose, status):
- Data contracts (schemas, retention, privacy):

## Release Scope
| Capability | API Endpoint | Owner | Notes |
|------------|--------------|-------|-------|

## Implementation Notes
- Dependencies:
- Open questions:
- Rollout strategy:

_Last updated: YYYY-MM-DD_
