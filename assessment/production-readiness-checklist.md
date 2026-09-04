# Production Readiness Checklist

Use this as the final go/no-go review before publishing or enabling an enterprise Copilot Studio agent in production.

## Ownership and approvals
- [ ] Business owner approved production release.
- [ ] Technical/platform owner approved production release.
- [ ] Security/compliance approval completed when required by risk classification.
- [ ] Production support owner is identified.
- [ ] Release/change record is created if required.

## Production configuration
- [ ] Correct production environment is confirmed.
- [ ] Managed solution/version intended for production is identified.
- [ ] Required environment variables are populated.
- [ ] Connection references resolve to approved production connections.
- [ ] Service accounts/service principals are production-specific where required.
- [ ] Authentication settings match approved design.
- [ ] Sharing scope matches approved audience.
- [ ] Agent channels are intentionally enabled.

## Security validation
- [ ] Anonymous access status has been reviewed.
- [ ] Maker-provided credentials, if used, have explicit approval.
- [ ] Agent-wide organizational sharing, if used, has explicit approval.
- [ ] Knowledge authorization has been tested as a normal end user.
- [ ] Least privilege review is complete.
- [ ] DLP/data policies allow only intended connectors and knowledge sources.

## Quality validation
- [ ] Critical business scenarios pass.
- [ ] Negative and out-of-scope scenarios pass.
- [ ] Action failures are handled acceptably.
- [ ] Knowledge citations/links are valid where expected.
- [ ] User acceptance testing is complete.
- [ ] Known limitations are documented for users/support.

## Operations
- [ ] Monitoring owner has access to required analytics.
- [ ] Transcript access is limited appropriately.
- [ ] Incident process is documented.
- [ ] Rollback/disable procedure is documented and tested where practical.
- [ ] Support contact is published.
- [ ] First production review date is scheduled.

## Decision

- [ ] GO
- [ ] GO WITH CONDITIONS
- [ ] NO-GO

**Approver:**  
**Date:**  
**Conditions:**
