# Connector Review Checklist

For every connector, flow, tool, custom connector, MCP server, or external API used by the agent:

- [ ] Business purpose is documented.
- [ ] Connector is allowed by organizational data policy/DLP.
- [ ] Data entering and leaving the connector is understood.
- [ ] Read vs write privileges are documented.
- [ ] Runtime credential model is documented.
- [ ] End-user credentials are preferred when user-context authorization is required.
- [ ] Maker-provided/shared credentials are explicitly reviewed.
- [ ] Service principal/service account permissions follow least privilege.
- [ ] Secrets are stored in approved secret-management locations.
- [ ] Production connections are not dependent on a personal maker account unless explicitly accepted.
- [ ] API rate limits, quotas, timeouts, and retry behavior are understood.
- [ ] Failure behavior does not expose secrets or sensitive payloads.
- [ ] Destructive/high-impact operations include appropriate validation or confirmation.
- [ ] Connector owner and support contact are documented.
