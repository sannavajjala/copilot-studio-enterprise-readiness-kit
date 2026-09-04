# Copilot Studio Enterprise Reference Architecture

This reference architecture is intentionally conceptual. It highlights control boundaries that should be understood before production deployment.

```text
                         ENTERPRISE USERS
                               |
                               v
                    +---------------------+
                    | Approved Channel(s) |
                    | Teams / M365 / Web  |
                    +----------+----------+
                               |
                         Authentication
                               |
                               v
                    +---------------------+
                    | Copilot Studio      |
                    | Enterprise Agent    |
                    +----+-----------+----+
                         |           |
              Knowledge  |           | Actions / Tools
                         |           |
             +-----------v--+     +--v----------------+
             | Enterprise   |     | Power Automate /  |
             | Knowledge    |     | Connectors / APIs |
             +------+-------+     +---------+---------+
                    |                       |
             Authorization              Runtime identity
                    |                       |
        +-----------v----------+     +------v-----------+
        | SharePoint / Fabric  |     | Dataverse / LOB  |
        | Dataverse / approved |     | SaaS / custom API|
        | enterprise sources   |     +------------------+
        +----------------------+

   -------------------------------------------------------------
   Cross-cutting controls:
   Environments | DLP/Data Policies | Identity | ALM | Monitoring
   Sharing | Audit/Transcripts | Support | Incident Response
   -------------------------------------------------------------
```

## Environment pattern

```text
Development  --->  Test / UAT  --->  Production
     |                 |                 |
 makers/test       business UAT      controlled users
 non-prod creds    target-like auth   prod identities
 unmanaged work    release candidate  managed/released artifact
```

## Architecture decisions to document

1. **Who can use the agent?**
2. **How are users authenticated?**
3. **What enterprise data can the agent retrieve?**
4. **Does source authorization follow the user, or does the agent use a shared identity?**
5. **What actions can the agent execute?**
6. **What identity executes each action?**
7. **What could happen if an action is wrong or abused?**
8. **How is the agent promoted between environments?**
9. **How is configuration separated by environment?**
10. **How will production behavior be monitored and supported?**

## Preferred enterprise pattern

For most internal enterprise agents, prefer:

- Microsoft Entra authenticated access.
- Narrow sharing through approved groups.
- User-context authorization for user-specific enterprise data where supported and appropriate.
- Dedicated service identities only where a shared application identity is genuinely needed.
- Solution-aware ALM with Dev/Test/Prod promotion.
- Environment-specific connection references and configuration.
- Explicit post-deployment publish/share validation.
- Monitoring ownership from day one.

The correct architecture depends on the use case. A low-risk informational agent and a high-impact transactional agent should not face identical controls.
