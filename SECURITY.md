# Security Policy

This policy covers the JABB platform: the mobile app for evaluators, the web dashboards for business clients and administrators, the public marketing site, the public API, the published CLI package, and the MCP server.

## Reporting a vulnerability

Use **GitHub private vulnerability reporting** on this repository: open the **Security** tab, then **Report a vulnerability**. The report is visible only to maintainers, and it stays private until we publish an advisory.

Do not open a public issue, and do not describe the vulnerability in a pull request or commit message.

Include what you have:

- Which component, and which environment — production, a preview deployment, or a local build
- What an attacker gains: data read, data written, privilege gained, availability lost
- Steps to reproduce, or a proof-of-concept request
- Whether you accessed, modified, or exfiltrated any real data while testing

**Never paste a live credential into a report.** Redact to the last four characters (`…7hHj`). If a key is exposed, say where it is exposed and treat it as compromised — rotating the key is what revokes it; deleting the file that held it does not.

## What to expect

| Stage | Target |
|---|---|
| Acknowledgement | 48 hours |
| Initial triage and severity call | 5 business days |
| Fix or documented mitigation | Severity-dependent, communicated at triage |

There is no bug bounty. Reporters who ask to be credited will be credited in the advisory.

## Scope

In scope: authentication and session handling, the reward economy and its anti-farming controls, the public API and MCP server, access-control and tenancy boundaries between business accounts, and any exposed credential or misconfigured cloud resource belonging to JABB.

Out of scope:

- Findings against third-party services we consume — report those to the vendor
- Missing hardening headers with no demonstrated impact
- Automated scanner output with no proof of exploitability
- Social engineering of staff or contractors
- **Denial-of-service and load testing against production.** Do not run them. A finding is not worth degrading service for real users.

## Handling personal data

JABB processes evaluator and employee data. Employee-experience submissions carry explicit privacy guarantees to the people who wrote them, including a contractual exclusion from disciplinary use.

If a finding exposes personal data: stop at the minimum proof needed, do not download or retain it, and say so in the report. Treat any exposure of employee-experience data as high severity regardless of how few records are involved.
