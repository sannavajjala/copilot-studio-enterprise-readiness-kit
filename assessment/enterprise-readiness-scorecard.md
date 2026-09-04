# Copilot Studio Enterprise Readiness Scorecard

Use this as an architecture and production-gate aid. It does not replace organization-specific security, privacy, legal, compliance, or risk review.

| Domain | Points |
|---|---:|
| Governance | 15 |
| Architecture | 10 |
| Identity | 15 |
| Data & Knowledge | 15 |
| Actions & Connectors | 10 |
| ALM | 15 |
| Security | 10 |
| Operations | 10 |
| **Total** | **100** |

Score full points when implemented with evidence, half points when partial, and zero when missing/unknown.

## Governance — 15
- [ ] **3** Purpose, intended users, and measurable outcome documented.
- [ ] **3** Business and technical/operational owners named.
- [ ] **3** Risk classification and reviewers documented.
- [ ] **3** Sharing/channel scope approved.
- [ ] **3** Data, connector, compliance, retention, and lifecycle requirements reviewed.

## Architecture — 10
- [ ] **2** Runtime architecture/dependencies documented.
- [ ] **2** Environment strategy and production boundary defined.
- [ ] **2** Knowledge, actions, flows, APIs, and downstream systems inventoried.
- [ ] **2** Failure modes/dependency limits considered.
- [ ] **2** Material capacity/performance assumptions tested.

## Identity — 15
- [ ] **3** End-user authentication is appropriate.
- [ ] **3** Production identities/service accounts identified.
- [ ] **3** End-user vs maker-provided credential model reviewed.
- [ ] **3** Maker/admin permissions follow least privilege.
- [ ] **3** Ownership transfer and credential lifecycle addressed.

## Data & Knowledge — 15
- [ ] **3** Knowledge sources have accountable owners.
- [ ] **3** Data classification/sensitivity known.
- [ ] **3** Restricted content tested with authorized and unauthorized personas.
- [ ] **3** Knowledge-source types comply with policy.
- [ ] **3** Grounding quality, stale-content risk, citations, and maintenance reviewed.

## Actions & Connectors — 10
- [ ] **2** Actions/connectors/flows/APIs/HTTP endpoints inventoried.
- [ ] **2** Data policy/DLP compatibility verified.
- [ ] **2** High-impact actions have appropriate authorization/approval controls.
- [ ] **2** Secrets/credentials are handled appropriately.
- [ ] **2** Failure, retry, duplicate-execution, and timeout behavior considered.

## ALM — 15
- [ ] **3** Dev/Test/Prod lifecycle defined.
- [ ] **3** Solution-aware components/dependencies identified.
- [ ] **3** Environment-specific connections/configuration validated.
- [ ] **3** Approved repeatable deployment process/pipeline used.
- [ ] **3** Preflight, smoke test, validation, versioning, and rollback documented.

## Security — 10
- [ ] **2** Copilot Studio security findings reviewed.
- [ ] **2** Authentication and authorization tested.
- [ ] **2** Sharing/publishing follows least access.
- [ ] **2** Exfiltration paths through knowledge/tools/connectors/channels/HTTP reviewed.
- [ ] **2** Privileged dependencies receive required security approval.

## Operations — 10
- [ ] **2** Production support owner/escalation path documented.
- [ ] **2** Monitoring and failure-review responsibilities assigned.
- [ ] **2** Incident containment/disable/unpublish procedure documented.
- [ ] **2** Usage, effectiveness, failures, and knowledge quality reviewed.
- [ ] **2** Periodic access/owner/dependency/configuration review scheduled.

# Result
**TOTAL: ____ / 100**

- **90–100:** READY
- **75–89:** READY WITH CONDITIONS
- **0–74:** NOT READY

## Critical-control override
A score cannot compensate for an unresolved critical risk. Examples:
- No accountable production owner.
- Authentication is inappropriate for the data/use case.
- Restricted knowledge authorization has not been validated.
- Production credential model creates an unaccepted privilege risk.
- Sharing exposes the agent beyond the approved audience.
- A high-impact action lacks required authorization/control.
- A known critical security/compliance issue remains unresolved.
- No viable containment/rollback approach exists for a material-risk agent.

A critical blocker should normally result in **NOT READY** until resolved or formally risk-accepted.

## Evidence
| Finding / control | Evidence | Owner | Due date |
|---|---|---|---|
| | | | |

## Approval
- Assessment date:
- Assessor:
- Business owner:
- Technical owner:
- Final result:
- Conditions/exceptions:
- Approver:
