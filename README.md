# Copilot Studio Enterprise Readiness Kit

> A practical, community-driven toolkit for evaluating whether Microsoft Copilot Studio agents are ready for enterprise deployment.

The **Copilot Studio Enterprise Readiness Kit** is a set of architecture, governance, security, ALM, deployment, and operational checklists designed for enterprise architects, platform administrators, makers, security teams, and agent owners.

This repository is intentionally **not** a software framework. It is a Monday-morning toolkit: documents you can copy, adapt, review in a design meeting, attach to a change ticket, or use as gates before an agent reaches production.

## Why this project exists

Enterprise agents fail for reasons that have little to do with prompt quality. Common problems include unclear ownership, over-broad sharing, inappropriate authentication, excessive connector permissions, unreviewed knowledge sources, unmanaged deployments, environment-specific connection failures, missing rollback plans, and no operational owner after launch.

This kit turns those concerns into repeatable review steps.

## Assess Your Agent

Use the [Enterprise Readiness Scorecard](assessment/enterprise-readiness-scorecard.md) to evaluate an agent across eight domains and produce a 100-point readiness result.

| Score | Result |
|---|---|
| 90–100 | READY |
| 75–89 | READY WITH CONDITIONS |
| 0–74 | NOT READY |

Critical security, identity, knowledge-access, sharing, action, ownership, or rollback failures can override the numerical score.

- [Start the assessment](assessment/enterprise-readiness-scorecard.md)
- [Scoring methodology](assessment/scoring-methodology.md)
- [Microsoft reference map](docs/microsoft-reference-map.md)

> Community-maintained decision support; not a Microsoft certification, security guarantee, or compliance attestation.


## What is included

| Area | Purpose |
|---|---|
| `assessment/` | Determine whether an agent is ready to move toward production |
| `governance/` | Intake, risk classification, sharing, and connector governance |
| `alm/` | Dev/Test/Prod, deployment preflight, validation, and rollback |
| `security/` | Identity, enterprise knowledge, and least-privilege reviews |
| `operations/` | Monitoring, incidents, ownership, and support readiness |
| `architecture/` | Reference architecture and enterprise design principles |
| `samples/` | Completed examples showing how to use the kit |

## Recommended enterprise lifecycle

```text
Idea / Request
     |
     v
Agent Intake
     |
     v
Risk Classification
     |
     v
Architecture + Security Review
     |
     v
Build in Development
     |
     v
Functional + Security Testing
     |
     v
Deployment Preflight
     |
     v
Test / UAT
     |
     v
Production Approval
     |
     v
Production Deployment
     |
     v
Post-Deployment Validation
     |
     v
Monitoring + Continuous Review
```

## Start here

If you are evaluating an existing agent, begin with:

1. [`assessment/agent-readiness-checklist.md`](assessment/agent-readiness-checklist.md)
2. [`governance/risk-classification-matrix.md`](governance/risk-classification-matrix.md)
3. [`assessment/production-readiness-checklist.md`](assessment/production-readiness-checklist.md)

If you are preparing a release, use:

1. [`alm/deployment-preflight.md`](alm/deployment-preflight.md)
2. [`alm/post-deployment-validation.md`](alm/post-deployment-validation.md)
3. [`alm/rollback-checklist.md`](alm/rollback-checklist.md)

If you administer the platform, focus on:

- [`governance/sharing-review-checklist.md`](governance/sharing-review-checklist.md)
- [`governance/connector-review-checklist.md`](governance/connector-review-checklist.md)
- [`security/identity-review.md`](security/identity-review.md)
- [`security/knowledge-access-review.md`](security/knowledge-access-review.md)
- [`operations/monitoring-checklist.md`](operations/monitoring-checklist.md)

## Readiness rating

Use a simple three-level outcome for reviews:

- **READY** — Required controls are satisfied; production deployment may proceed.
- **READY WITH CONDITIONS** — Deployment may proceed only after documented exceptions, compensating controls, or time-bound remediation are approved.
- **NOT READY** — One or more critical controls are missing or unacceptable.

### Suggested critical blockers

An agent should normally be considered **NOT READY** when any of the following apply:

- No accountable business owner or technical owner.
- Production authentication model is undefined.
- Sensitive knowledge can be accessed without appropriate authorization.
- Production connectors or actions use credentials that have not been security-reviewed.
- Sharing scope is broader than the approved audience.
- Required production connection references, environment variables, or service identities are unresolved.
- No rollback or disablement path exists.
- No monitoring/support owner exists for production.

## Guiding principles

### 1. Identity before intelligence
An agent should never be trusted with enterprise data or actions until its user identity, service identity, and authorization behavior are understood.

### 2. Least privilege by default
Grant the smallest audience, connector access, knowledge access, and runtime permissions needed for the use case.

### 3. Environment separation matters
Use controlled Development, Test/UAT, and Production environments for enterprise agents. Avoid building production-critical agents directly in production.

### 4. Deploy repeatably
Package agent components in solutions and use a repeatable deployment mechanism. Treat connections, environment variables, dependencies, and post-deployment publishing as release concerns.

### 5. Production is an operational commitment
An agent is not production-ready until someone owns monitoring, incidents, access reviews, content changes, and retirement.

## Microsoft platform alignment

The kit is designed to align with current Microsoft Copilot Studio and Power Platform capabilities, including:

- Power Platform solutions and deployment pipelines for ALM.
- Microsoft Entra ID-based authentication patterns.
- Data policies for controlling connectors, authentication patterns, and knowledge source types.
- Copilot Studio sharing controls for users, security groups, collaborators, and analytics viewers.
- Copilot Studio Monitor/Analytics, transcripts, feedback, and agent-flow monitoring.

Microsoft features change frequently. Treat this repository as an implementation aid, not a replacement for Microsoft documentation, your security standards, legal/compliance review, or organizational policy.

## Version 0.1 scope

The first release focuses on **enterprise readiness reviews** rather than automation. Future community contributions may add reusable examples such as:

- Power Platform pipeline validation patterns
- Environment strategy examples
- PowerShell or CLI validation scripts
- Sample architecture decision records
- Sample exception register
- Agent inventory templates

The project should remain lightweight. Automation belongs here only when it makes the readiness process easier to use.

## Contributing

Contributions are welcome. Useful contributions include:

- Additional checklist controls backed by a real enterprise deployment scenario
- Improvements to risk classification
- Platform-specific examples
- Corrections when Microsoft capabilities change
- Sample completed assessments with fictionalized data

When proposing a new control, explain the failure mode it is intended to prevent.

## Disclaimer

This project is community-created and is not an official Microsoft product. Microsoft, Copilot, Copilot Studio, Power Platform, Power Automate, Power Apps, Microsoft Fabric, and Microsoft Entra are trademarks of Microsoft Corporation.

## License

Released under the [MIT License](LICENSE).
