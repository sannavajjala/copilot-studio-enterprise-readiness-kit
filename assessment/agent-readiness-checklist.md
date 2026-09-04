# Agent Readiness Checklist

Use this checklist during architecture/design review before an enterprise Copilot Studio agent enters formal production-readiness testing.

**Agent:**  
**Business owner:**  
**Technical owner:**  
**Environment:**  
**Reviewer:**  
**Date:**

## Business readiness

- [ ] Business problem is documented.
- [ ] Expected users and audience are defined.
- [ ] Business owner is accountable for the agent's outcomes.
- [ ] Technical/platform owner is identified.
- [ ] Success metrics are defined.
- [ ] Out-of-scope scenarios are documented.
- [ ] Human escalation path exists where appropriate.
- [ ] Agent retirement criteria are understood.

## Data and knowledge

- [ ] Every knowledge source has a named owner.
- [ ] Knowledge sources are approved for the intended audience.
- [ ] Sensitive/confidential data classification is documented.
- [ ] Access behavior has been tested using non-owner accounts.
- [ ] Stale, duplicate, draft, or unapproved content is excluded where necessary.
- [ ] Public web knowledge is intentionally enabled or intentionally blocked.
- [ ] Expected citations/source links have been validated.

## Identity and access

- [ ] User authentication model is documented.
- [ ] Anonymous access is either prohibited or explicitly approved for the use case.
- [ ] Sharing audience is limited to approved users/security groups.
- [ ] Co-author permissions are limited to authorized makers/admins.
- [ ] Runtime identities for connectors/actions are understood.
- [ ] Service accounts/service principals have accountable owners.
- [ ] Credentials are not embedded in instructions, variables, topics, or documentation.

## Actions and connectors

- [ ] Every action has a clear business purpose.
- [ ] Connector data classification is compatible with organizational DLP policy.
- [ ] Write/delete/update actions have stronger review than read-only actions.
- [ ] High-impact actions include validation or confirmation where appropriate.
- [ ] Error and timeout behavior has been tested.
- [ ] External API dependencies and rate limits are documented.
- [ ] Connection ownership will survive employee role changes or departures.

## Agent behavior

- [ ] Instructions define the agent's purpose and boundaries.
- [ ] Agent has been tested for unsupported/out-of-scope requests.
- [ ] Agent does not claim access or capabilities it does not have.
- [ ] Sensitive actions are not triggered solely from ambiguous user intent.
- [ ] Failure messages give users a meaningful next step.
- [ ] Safety/escalation behavior is documented for relevant scenarios.

## Platform and lifecycle

- [ ] Agent is developed in an approved environment.
- [ ] Agent and dependencies are included in an appropriate solution.
- [ ] Dev/Test/Prod promotion path is defined.
- [ ] Environment-specific values are externalized where possible.
- [ ] Production connection references are known.
- [ ] Deployment ownership is documented.
- [ ] Monitoring/support plan exists.

## Outcome

**Readiness:** READY / READY WITH CONDITIONS / NOT READY

**Conditions / blockers:**

1. 
2. 
3. 
