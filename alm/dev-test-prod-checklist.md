# Dev / Test / Prod Checklist

## Development
- [ ] Development occurs in an approved non-production environment.
- [ ] Agent is created inside or added to an appropriate solution.
- [ ] Dependencies are solution-aware where supported.
- [ ] Environment variables are used for environment-specific configuration where appropriate.
- [ ] Connection references are used consistently.
- [ ] Makers do not use production credentials for routine development.

## Test / UAT
- [ ] Deployment uses the same promotion mechanism intended for production.
- [ ] Test connections resolve correctly.
- [ ] Test identities approximate production security behavior.
- [ ] Business UAT covers critical scenarios.
- [ ] Sharing is limited to the UAT population.
- [ ] Defects and deployment-specific fixes are captured in source development rather than manually patched only in test.

## Production
- [ ] Production uses managed artifacts where required by organizational ALM standards.
- [ ] Deployment is performed by an approved deployment identity/process.
- [ ] Production configuration is not manually drifted without documentation.
- [ ] Publishing/enabling channels is included in the release procedure.
- [ ] Version and release date are recorded.
- [ ] Post-deployment validation is completed.
