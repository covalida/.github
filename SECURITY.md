# Security Policy

## Supported Versions

Security fixes are applied to the **latest `main` branch only**. We do not backport to older releases.

| Repository | Supported |
|-----------|-----------|
| `platform` | ✅ `main` |
| `cb-engine` | ✅ `main` |
| `geo-pipeline` | ✅ `main` |
| `ec-rep` | ✅ `main` |
| `infra` | ✅ `main` |
| All others | ✅ `main` |

---

## Reporting a Vulnerability

**Do not open a public GitHub issue for security vulnerabilities.**

Report to: **[security@covalida.com](mailto:security@covalida.com)**

Please include:

- **Affected repository** and branch / version / commit hash
- **Vulnerability description** — type (e.g. IDOR, SQLi, XSS, path traversal), affected component, attack vector
- **Potential impact** — data exposure, privilege escalation, compliance data integrity, etc.
- **Steps to reproduce** — minimal proof-of-concept if available
- **Suggested mitigation** (optional)

You will receive:
- **Acknowledgement within 48 hours**
- **Status update within 7 business days**

---

## Disclosure Policy

We follow **Coordinated Vulnerability Disclosure (CVD)**:

1. Reporter submits findings privately to `security@covalida.com`
2. We acknowledge receipt within 48 h
3. We assess severity and assign internal tracking
4. We develop and test a fix — target SLA:
   - **Critical / High (CVSS ≥ 7.0):** ≤ 14 days
   - **Medium (CVSS 4.0–6.9):** ≤ 45 days
   - **Low (CVSS < 4.0):** ≤ 90 days
5. Fix is released and deployed
6. Public disclosure coordinated with reporter; reporter credited unless anonymity is requested

We ask reporters to refrain from public disclosure until the fix is deployed or until 90 days have elapsed from initial report (whichever comes first), in line with [Google Project Zero](https://googleprojectzero.blogspot.com/p/vulnerability-disclosure-faq.html) norms.

---

## Scope

### In scope

- Authentication, session management, and OIDC/OAuth flows
- Authorization and RBAC flaws (tenant isolation, role escalation)
- Data exposure — especially GDPR-relevant personal data
- CB workflow integrity (application, audit, decision, certificate lifecycle)
- Traceability and chain-of-custody data manipulation
- Geo-pipeline data integrity (EUDR deforestation evidence)
- EC-REP legal document custody and access control
- Injection vulnerabilities (SQL, command, SSRF, template)
- Secrets exposure in code or CI artifacts

### Out of scope

- Third-party dependencies — report upstream to the respective project
- Social engineering or phishing against Covalida staff
- Physical security
- Denial-of-service / DDoS
- Automated scanner output without manual verification and proof of impact
- Theoretical vulnerabilities without demonstrated exploit path

---

## GDPR Relevance

Covalida processes personal data subject to GDPR and operates certification workflows with legal standing. Vulnerabilities that may expose personal data, compromise audit trails, or undermine certificate integrity are treated with highest internal priority and may trigger breach notification obligations under Art. 33 GDPR.

---

## PGP / Encrypted Communication

A PGP public key and `security.txt` are available at:

[https://covalida.com/.well-known/security.txt](https://covalida.com/.well-known/security.txt)

---

## Hall of Thanks

We gratefully acknowledge responsible disclosures. Reporters who wish to be credited will be listed here after fix deployment.

| Reporter | Finding | Year |
|---------|---------|------|
| — | — | — |
