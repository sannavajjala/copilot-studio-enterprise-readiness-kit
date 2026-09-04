# Rollback Checklist

A rollback plan should answer: **How do we stop harm quickly, then restore service safely?**

## Immediate containment options
- [ ] Unpublish/disable the agent or affected channel if appropriate.
- [ ] Disable a failing/high-risk flow or action.
- [ ] Remove/restrict sharing if access is the issue.
- [ ] Revoke or rotate compromised credentials.
- [ ] Remove an unsafe knowledge source.

## Restore previous state
- [ ] Previous known-good solution/version is available.
- [ ] Previous configuration values are documented.
- [ ] Previous connection mappings are known.
- [ ] Data changes caused by the failed release have been assessed separately from application rollback.
- [ ] Backout deployment procedure is documented.

## Validation after rollback
- [ ] Agent behavior matches previous known-good state.
- [ ] Security/sharing configuration is correct.
- [ ] Critical actions are functioning.
- [ ] Monitoring confirms recovery.
- [ ] Incident/change record documents cause, rollback, and follow-up actions.
