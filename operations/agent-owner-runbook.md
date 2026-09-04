# Agent Owner Runbook

## Ownership
**Agent:**  
**Business owner:**  
**Technical owner:**  
**Support team:**  
**Knowledge owner(s):**

## Production locations
- Environment:
- Solution:
- Agent URL/reference:
- Supported channels:
- Sharing group(s):

## Dependencies
- Knowledge sources:
- Flows/actions:
- Connectors/APIs:
- Service identities:
- Environment variables:

## Routine checks
### Weekly / biweekly
- Review failures and major user-reported issues.
- Review action-run failures.

### Monthly
- Review usage, feedback, answer-quality concerns, and knowledge freshness.
- Confirm owner/support contacts remain valid.

### Quarterly or policy cadence
- Review sharing/access.
- Review service identity permissions.
- Review connector inventory.
- Reconfirm business value and production need.

## Common failure modes
| Symptom | First checks |
|---|---|
| Agent unavailable | Publication/channel status, environment, service health |
| User denied | Authentication, sharing, source permissions |
| Maker works but user fails | User identity, connection ownership, source authorization |
| Action fails | Flow/activity logs, connection reference, credential, API availability |
| Wrong/stale answer | Knowledge source, source freshness, agent instructions |

## Emergency actions
Document who is authorized to disable the agent, restrict sharing, disable actions, and rotate credentials.
