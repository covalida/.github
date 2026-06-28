# Contributing to Covalida

Thank you for considering a contribution. This guide applies across all Covalida repositories unless a repository provides its own `CONTRIBUTING.md`.

Before you start: read and accept our [Code of Conduct](CODE_OF_CONDUCT.md).  
For security vulnerabilities, follow [SECURITY.md](SECURITY.md) — do **not** open a public issue.

---

## Development Prerequisites

| Tool | Version |
| --- | --- |
| Node.js | ≥ 24 LTS |
| pnpm | ≥ 10 |
| Docker + Docker Compose | latest stable |
| Python | ≥ 3.14 (geo-pipeline only) |
| kubectl | ≥ 1.34 (infra / k8s work) |

---

## Quick Start

```bash
# 1. Clone
git clone https://github.com/covalida/<repo-name>.git
cd <repo-name>

# 2. Install dependencies
pnpm install

# 3. Configure environment
cp .env.example .env.local
# Edit .env.local — see repo-specific README for required values

# 4. Start backing services (Postgres, RabbitMQ)
docker compose -f docker-compose.dev.yml up -d

# 5. Start dev server
pnpm dev
```

Repo-specific setup instructions live in the respective `README.md`.

---

## Branching Strategy

We use **trunk-based development** with short-lived feature branches.

| Branch pattern | Purpose |
| --- | --- |
| `main` | Production-ready. Protected — direct pushes blocked. |
| `development` | Integration branch. CI runs on every push. |
| `feature/<ticket-id>-short-description` | Feature work |
| `fix/<ticket-id>-short-description` | Bug fixes |
| `chore/<description>` | Maintenance, dependency updates |
| `hotfix/<description>` | Emergency production fixes (branch from `main`) |

Branch names use lowercase kebab-case. Keep them short and descriptive.

---

## Commit Conventions

We follow [Conventional Commits](https://www.conventionalcommits.org/) strictly — it drives our changelog and version bumps.

```
<type>(<scope>): <subject>

[optional body]

[optional footer(s)]
```

**Types:** `feat` · `fix` · `docs` · `style` · `refactor` · `perf` · `test` · `build` · `ci` · `chore` · `revert`

**Scopes:** `platform` · `cb-engine` · `geo` · `ec-rep` · `auth` · `api` · `ui` · `infra` · `deps`

Breaking changes require `BREAKING CHANGE:` in the footer, or `!` after the type (`feat!:`).

Examples:
```
feat(cb-engine): add ISO 17065 application lifecycle state machine
fix(geo): handle null geometry in Sentinel-2 intersection query
chore(deps): bump Astro to 6.x
feat!: remove deprecated v1 REST API endpoints
```

---

## Pull Request Process

1. Branch off `dev` (or `main` for hotfixes)
2. One concern per PR — avoid mixing unrelated changes
3. All CI checks must pass before requesting review
4. Fill in the PR template completely
5. Minimum **1 approving review** required; **2** for `main` merges
6. Default merge strategy: **squash merge** into `main`

### Regulatory Co-review

PRs touching CB engine, traceability, geo-pipeline, or EC-REP modules require an additional review from the compliance team. The PR template has a checklist for this.

---

## Code Style

- **TypeScript**: strict mode, no untyped `any` without explicit justification in a comment
- **Formatting**: Prettier (config committed at repo root)
- **Linting**: ESLint with project config
- **Pre-commit**: Husky + lint-staged enforces formatting automatically

Run checks manually:
```bash
pnpm lint        # ESLint
pnpm typecheck   # tsc --noEmit
pnpm format      # Prettier check
```

---

## Testing

| Type | Tool | Required? |
| --- | --- | --- |
| Unit | Vitest | Yes |
| Integration / E2E | Playwright | Yes (platform repo) |
| Geo pipeline | pytest + PostGIS fixtures | Yes (geo-pipeline repo) |
| API contract | Bruno / OpenAPI | Recommended |

```bash
pnpm test          # Unit tests
pnpm test:e2e      # End-to-end (requires running dev stack)
pnpm test:coverage # Coverage report
```

New features must ship with tests. Bug fixes must include a regression test.

---

## Architecture Decisions

Significant architectural changes require an **Architecture Decision Record (ADR)** in `50.3.4` of our internal documentation before implementation. Reference the ADR number in your PR description.

---

## Regulatory Sensitivity

Covalida code may directly underpin **accredited certification activities** (ISO/IEC 17065, 17021, 17024) and **legally mandated EU compliance workflows** (EUDR, LkSG, CSDDD). Any change affecting:

- CB workflow lifecycle (application → audit → decision → certificate)
- Traceability records or chain-of-custody data
- Geo-data integrity (EUDR deforestation checks)
- EC-REP legal document custody

…must include the compliance team as a reviewer, reference the relevant regulation in the PR description, and may require an ADR if it alters behaviour.

---

## Questions

[Open a Discussion](https://github.com/orgs/covalida/discussions) or write to [hello@covalida.com](mailto:hello@covalida.com).
