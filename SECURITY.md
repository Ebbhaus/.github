# Security

Internal security process for Ebbhaus engineers. If you're not an Ebbhaus
employee or contractor, you shouldn't be reading this.

## Reporting a security issue

If you find or suspect a vulnerability, misconfiguration, leaked credential,
or suspected compromise in any Ebbhaus system:

1. **Post in `#eng-security` on Slack** with a short description.
2. Page the on-call security engineer if it looks active or high severity.
3. Do **not** file a public-style GitHub issue with details. Track the work in
   a private issue or ticket linked from the Slack thread.

## Severity guide

- **SEV-1**: Active exploitation, customer data at risk, auth bypass, secret
  leak to the public internet. Page on-call immediately.
- **SEV-2**: Exploitable but not active, or limited blast radius. Same-day
  response.
- **SEV-3**: Hardening, best-practice gaps, low-impact issues. Track as a
  normal ticket.

## Credential leaks

If you accidentally commit or expose a secret:

1. Rotate the secret **first**, before anything else.
2. Post in `#eng-security`.
3. Don't just force-push to erase the commit — assume it was scraped.

## Third-party reports

If an external researcher contacts us about a vulnerability, route them to
`security@ebbhaus.com` and loop in `#eng-security`. Don't engage on the
technical details yourself until security has triaged.
