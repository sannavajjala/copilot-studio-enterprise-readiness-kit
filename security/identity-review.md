# Identity Review

## End-user identity
- [ ] Authentication method is documented.
- [ ] Microsoft Entra authentication is used when enterprise identity is required.
- [ ] Anonymous access is justified and approved if enabled.
- [ ] Authorization assumptions are tested with representative users.

## Runtime identity
- [ ] Each connector/action runtime identity is documented.
- [ ] It is clear whether actions run as the end user, maker/shared account, service account, or service principal.
- [ ] Shared identities have named owners.
- [ ] Shared identities are not personal employee accounts.
- [ ] MFA/conditional-access/service-account treatment follows organizational policy.
- [ ] Service principal permissions are scoped to required resources.

## Lifecycle
- [ ] Credential rotation process exists where applicable.
- [ ] Offboarding an agent owner will not unexpectedly break production.
- [ ] Emergency credential revocation is possible.
- [ ] Identity dependencies are documented in the owner runbook.
