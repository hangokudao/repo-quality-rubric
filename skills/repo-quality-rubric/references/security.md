# Security Overlay

Use this for repos with authentication, authorization, payments, user data, network actions, file deletion, deployment, or public package distribution.

## Checks

- Secrets: no API keys, tokens, `.env` values, private certs, or personal credentials are committed.
- Authorization: external targets, destructive actions, and data transmission require explicit authorization.
- Dependencies: dependency files are present and lockfiles are consistent; audit only when safe and relevant.
- Inputs: untrusted input is validated before shell, file, SQL, HTML, or network use.
- Outputs: logs and reports do not expose secrets or private data.
- Supply chain: package publish contents are clean; build scripts are not surprising; provenance/CI is understandable when important.
- Web/API: use OWASP-style checks for auth, session handling, access control, validation, file upload, and error disclosure.

## Deductions

- Secrets or private data are present in current files: critical.
- Tool can mutate external targets without explicit authorization: high or critical.
- Security claims exist without tests, docs, or guardrails: medium to high.
- Dependency or publish workflow is opaque for a public package: medium.

## Useful External Baselines

- OpenSSF Scorecard for open source supply-chain hygiene.
- OWASP ASVS for web/API verification.
- OWASP Top 10 for broad web application risk framing.
