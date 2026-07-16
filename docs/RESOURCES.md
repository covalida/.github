<!--
  SINGLE SOURCE OF TRUTH for all Covalida public contact addresses, web
  properties, and brand constants. Every other file in this repository
  (profile/README.md, SECURITY.md, CONTRIBUTING.md, CODE_OF_CONDUCT.md,
  SUPPORT.md, ISSUE_TEMPLATE/*) MUST match the canonical values below.
  When something changes, change it HERE first, then propagate.
-->

# Covalida — Contact & Resource Directory

> **Single source of truth.** This document is the authoritative registry of all
> Covalida email addresses, web properties, and brand constants referenced across
> this organization's repositories. If a value here disagrees with another file,
> **this file wins** — and the other file should be corrected.

---

## Web Properties

| URL | Purpose | Referenced in |
| --- | --- | --- |
| `https://covalida.com` | Primary website / corporate home | `profile/README.md`, `ISSUE_TEMPLATE/config.yml` |
| `https://covalida.com/s/ec-rep` | EU Authorized Representative (EC-REP) service | `profile/README.md`, `ISSUE_TEMPLATE/config.yml` |
| `https://trust.covalida.com` | Trust Center (certifications, sub-processors, status) | `profile/README.md` |
| `https://docs.covalida.com` | Public product & API documentation | `profile/README.md`, `CONTRIBUTING.md`, `ISSUE_TEMPLATE/config.yml` |
| `https://brand-guide.covalida.com` | Brand guide — corporate identity & downloadable assets | `docs/BRAND.md` |
| `https://covalida.com/s/imprint` | Legal notice (imprint) | `profile/README.md` |
| `https://covalida.com/s/privacy-policy` | Privacy policy | `profile/README.md` |
| `https://covalida.com/.well-known/security.txt` | `security.txt` + PGP public key (RFC 9116) | `SECURITY.md` |
| `https://github.com/covalida` | GitHub organization | this repo |
| `https://github.com/orgs/covalida/discussions` | Community discussions | `CONTRIBUTING.md`, `ISSUE_TEMPLATE/config.yml`, `SUPPORT.md` |

> **URL convention.** Marketing/legal sub-pages use the `/s/<slug>` path scheme
> (e.g. `/s/ec-rep`, `/s/imprint`, `/s/privacy-policy`). Do **not** introduce
> bare-path variants such as `/ec-rep` — they fragment the canonical link set.

---

## Email Addresses

| Address | Purpose | Response target | Referenced in |
| --- | --- | --- | --- |
| `hello@covalida.com` | General enquiries, community & business contact | — | `CONTRIBUTING.md`, `SUPPORT.md` |
| `compliance@covalida.com` | Compliance & accreditation enquiries (ISO/IEC 17065 / 17021 / 17024, EC-REP) | — | `profile/README.md`, `SUPPORT.md` |
| `security@covalida.com` | Security & coordinated vulnerability disclosure | Ack ≤ 48 h; status ≤ 7 business days | `SECURITY.md`, `ISSUE_TEMPLATE/config.yml`, `SUPPORT.md` |
| `conduct@covalida.com` | Code of Conduct reports (confidential) | — | `CODE_OF_CONDUCT.md` |

> **Do not invent role addresses.** Route new needs to one of the four above
> unless a new mailbox is provisioned and added here first.

---

## GitHub Presence

| Resource | Location |
| --- | --- |
| Organization | `https://github.com/covalida` |
| Community health repository | `https://github.com/covalida/.github` (this repo) |
| Discussions | `https://github.com/orgs/covalida/discussions` |
| Default code owners | `@covalida/core` |

> **How this repository works.** As the organization's special `.github`
> repository, the files here are **org-wide defaults**: `profile/README.md`
> renders on the organization landing page, and the community health files
> (`CONTRIBUTING.md`, `SECURITY.md`, `CODE_OF_CONDUCT.md`, `SUPPORT.md`,
> `ISSUE_TEMPLATE/`, `PULL_REQUEST_TEMPLATE.md`) are inherited as fallbacks by
> every repository in the organization that does not define its own.

---

## Brand Palette

| Token | Hex | Usage |
| --- | --- | --- |
| Deep Teal | `#008080` | Primary — brand color, key surfaces, primary emphasis |
| Light Teal | `#20B2AA` | Accent — lines, highlights, data-viz (not small text on white) |
| Deep Petrol | `#155D5B` | Deep — button backgrounds, icon circles, gradient end |
| Deep Slate Gray | `#2F4F4F` | Text — body copy, headings, and the wordmark |
| Light Mint | `#CDE9E6` | Surface — section backgrounds, calm fills |
| EU Blue | `#003399` | EU-flag accent — **EC-REP badge only**, not a brand color |
| EU Gold | `#FFCC00` | EU-flag accent — paired with EU Blue on the EC-REP badge |

Tagline: **"Securing the Core."** · Typeface: **Montserrat** (400–800).

> Full corporate identity (logo, construction grid, typography, scalability,
> usage rules) lives in [BRAND.md](BRAND.md); the authoritative brand guide with
> the complete asset library is at [brand-guide.covalida.com](https://brand-guide.covalida.com).

---

## Regulatory Scope (Service Pillars)

| Pillar | Regulatory scope |
| --- | --- |
| 🛡️ Core | GDPR · AI Act · NIS2 · ISO 27001 |
| 🔒 Tech & Trust | Cyber Resilience Act (CRA) · Product Safety · CE Marking · GSPR |
| 🔗 Traceability | LkSG · CSDDD · EUDR — supply-chain due diligence & chain of custody |
| ♻️ Circularity | PPWR · Digital Product Passport (DPP) · Ecodesign Regulation |
| 🎓 Training | ISO/IEC 17024 personnel certification · LMS platform |
| 🌍 EC-REP | EU Authorized Representative for non-EU manufacturers |

---

## Maintenance

- **Owner:** `@covalida/core`
- **Change rule:** Update a value here **first**, then propagate to every file
  listed in the "Referenced in" columns. Keep each address/URL canonical and
  spelled identically everywhere.
- **Verification:** Before committing changes that touch contacts or URLs, grep
  the repository for the old value to ensure no stray references remain.
