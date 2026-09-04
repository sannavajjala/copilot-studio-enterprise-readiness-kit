# Agent Risk Classification Matrix

Use this matrix to determine the depth of review required. Organizations should adapt thresholds to their own policy.

| Dimension | Low | Medium | High |
|---|---|---|---|
| Audience | Small internal group | Department/business unit | Organization-wide or external |
| Data | Public/internal | Confidential business data | Regulated, highly confidential, privileged |
| Actions | Read-only | Creates/updates low-impact records | Financial, HR, security, legal, destructive, irreversible |
| Identity | Entra-authenticated, user-scoped | Shared service identity with controls | Anonymous, external, broad privileged service identity |
| Knowledge | Curated low-risk sources | Multiple enterprise sources | Sensitive sources or complex authorization boundaries |
| Autonomy | User initiated | Scheduled/event driven with limited actions | Autonomous high-impact decisions/actions |
| Integrations | Standard approved systems | External APIs/line-of-business systems | Critical systems or elevated permissions |
| Business impact | Convenience/productivity | Operational dependency | Material financial, legal, safety, security, or reputational impact |

## Suggested classification

**Low risk**  
Mostly read-only, authenticated, small audience, non-sensitive information, low business impact.

**Medium risk**  
Enterprise data, departmental scale, write actions, service identities, or meaningful operational impact.

**High risk**  
Sensitive/regulated data, broad/external access, privileged actions, autonomous high-impact behavior, or material business consequences.

## Suggested review requirements

| Review | Low | Medium | High |
|---|:---:|:---:|:---:|
| Business owner approval | ✓ | ✓ | ✓ |
| Platform/admin review | ✓ | ✓ | ✓ |
| Security review | As needed | ✓ | ✓ |
| Privacy/compliance review | As needed | As needed | ✓ |
| Formal UAT | Recommended | ✓ | ✓ |
| Rollback plan | Basic | ✓ | ✓ |
| Post-launch review | 30–90 days | 30 days | 7–30 days |
