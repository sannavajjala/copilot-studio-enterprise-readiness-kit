# Example Agent Assessment — Engineering Knowledge Assistant

> Fictional example showing how the kit can be completed.

## Summary

**Purpose:** Allow authenticated engineering employees to ask questions over approved engineering procedures stored in SharePoint.  
**Audience:** Engineering security group (~450 users).  
**Actions:** None; read-only informational agent.  
**Risk:** Medium, because internal engineering content includes controlled procedures and incorrect answers could affect operations.

## Key decisions

- Authentication: Microsoft Entra authenticated.
- Sharing: Engineering security group only.
- Knowledge: Approved SharePoint libraries; no public websites.
- Runtime actions: None in v1.
- Environments: Development → QA/UAT → Production.
- Deployment: Solution-based promotion using approved Power Platform pipeline.
- Monitoring: Technical owner reviews analytics and reported failures; knowledge owners review content quality monthly.

## Readiness findings

| Area | Result | Notes |
|---|---|---|
| Business ownership | Pass | Engineering director is business owner |
| Authentication | Pass | Entra authenticated |
| Sharing | Pass | Engineering security group |
| Knowledge authorization | Conditional | Must test restricted library with non-member account |
| Connectors/actions | Pass | No transactional actions |
| ALM | Pass | Dev/QA/Prod path established |
| Monitoring | Pass | Support owner identified |
| Rollback | Pass | Agent can be unpublished and prior solution retained |

## Decision

**READY WITH CONDITIONS**

### Required before production
1. Validate that a user without permission to the restricted SharePoint library cannot retrieve content from it.
2. Complete production smoke test using a standard engineering-user account.
3. Record production sharing group and solution version in the owner runbook.
