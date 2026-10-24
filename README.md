# Tappix — Diploma Materials

**Development of an Information System for Managing Customer Relationships in Small Businesses Through Digital Loyalty Programs.**

Public review package for the first diploma submission, 24 October 2026.
This repository contains documentation and static designs, **not application source code**.
The original development repository and its history remain private; this publication does not replace them.

## Start here

- [English report — PDF (26 pages)](docs/report/en/Tappix-Pre-Defense-Report-EN.pdf)
- [Editable English report — Word](docs/report/en/Tappix-Pre-Defense-Report-EN.docx)
- [Six interface concepts](docs/prototype/README.md)
- [Architecture diagrams and editable sources](diagrams/README.md)
- [Submission requirements and outstanding items](SUBMISSION-STATUS.md)

![Guest wallet and progress concept](docs/prototype/guest-journey.png)

## Problem, users and expected outcomes

Small businesses may track visits and rewards using paper cards or manual records.
Tappix proposes a digital loyalty card accessed through a link, QR or NFC, a staff
scanner workflow, and an owner dashboard. The target market is small businesses in
Kazakhstan, including cafés, bakeries and salons. Problem frequency, demand,
willingness to pay and sales impact remain hypotheses requiring real-world validation.

| Role | Planned capability |
| --- | --- |
| Platform administrator | Connect businesses, assign plans, features, limits and a seven-day trial |
| Business owner | Manage branches, staff, loyalty rules, customer metrics and quota usage |
| Employee | Confirm visits, award points and redeem rewards within the employer's company |
| Guest | Store separate loyalty cards, view progress, history and available rewards |

The wallet is not a payment wallet. Points are business-defined rewards, not money.
Assigning a subscription plan does not record payment. Tenant isolation and
transactional, idempotent ledger operations are implementation requirements.

## Team and supervisor

| Student | Group | GitHub | Assigned responsibility |
| --- | --- | --- | --- |
| Armat Islambekov | SE-2403 | [islqdev](https://github.com/islqdev) | Frontend, Next.js, React, TypeScript, UX and charts |
| Kambekov Yersultan | SE-2417 | [Ersultan7](https://github.com/Ersultan7) | Backend, Go, PostgreSQL, Redis, Docker/Nginx and CI/CD |

**Supervisor:** Elvira Aitmukhanbetova.
Assigned responsibilities are not a claim that all work has been completed.
Personal reviews and contributions must be recorded through each student's own account.

## Scope and current status

Prepared: scope, requirements, literature review, product and technology comparisons,
three architecture diagrams, six static interface concepts, evaluation plan and English report.
The report references 12 scientific studies and 14 official sources.
The diagrams describe a proposed architecture; the images are design concepts with fictional data.
The diploma implementation is not yet a complete running application.

Planned core: company isolation, roles and sessions, visits/stamps, reward points,
discounts, guest wallet, owner analytics, administration, limits and trials.
Payment processing, partner transfers, campaigns, POS integration and AI features are
outside the first implementation scope. No production readiness or sales uplift is claimed.

AI-assisted role discussions are explicitly labelled simulations, not real interviews.
Teacher feedback relayed by Armat is recorded separately from simulated adviser dialogue.
Acceptance of the revised materials and peer review remain pending.

## Proposed technology

Next.js, React and TypeScript; Go REST/JSON with OpenAPI; PostgreSQL; Redis for
sessions, rate limits and temporary/background state; Docker and Nginx.
See [technology comparisons](docs/comparisons/README.md) and
[architecture decision](docs/ADR/0001-modular-monolith.md).

## Documentation

| Material | Link |
| --- | --- |
| Proposal and scope | [Scope](docs/proposal/README.md) |
| Literature | [Evidence register and critical review](docs/literature/README.md) |
| Existing products and technologies | [Comparisons](docs/comparisons/README.md) |
| Requirements and acceptance criteria | [Requirements](docs/requirements/README.md) |
| Verification and evaluation | [Evaluation plan](docs/requirements/evidence-and-evaluation.md) |
| Architectural decisions | [ADR](docs/ADR/0001-modular-monolith.md) |
| Diagrams | [DOT sources, PNG and SVG exports](diagrams/README.md) |
| Prototype | [Static concepts](docs/prototype/README.md) |
| Report | [English PDF](docs/report/en/Tappix-Pre-Defense-Report-EN.pdf) |
| Tasks, owners, acceptance and deadlines | [Work plan](tasks/plan.md) |

## Project tracking and access

- [YouTrack project](https://tappix-diploma.youtrack.cloud/issues/DIP)
- [YouTrack board](https://tappix-diploma.youtrack.cloud/agiles/204-1/218-1)
- [Private development repository](https://github.com/islqdev/tappix-diploma) — requires access.

YouTrack may also require authentication. Public documents do not automatically
provide access to the private development history or task tracker. Reviewer access
must be arranged separately if the university requires inspection of those records.

## View and verify

No installation is required: open the report and PNG previews directly on GitHub.
Download the Word file for editing. Editable diagrams use Graphviz DOT.

```sh
# Verify that the published files match their recorded checksums (Linux):
sha256sum --check SHA256SUMS
# macOS equivalent:
shasum -a 256 --check SHA256SUMS
# Regenerate one diagram if Graphviz is installed:
dot -Tpng diagrams/context.dot -o /tmp/tappix-context.png
```

The publication CI verifies file integrity and the absence of application directories.
It does not test an application or prove security. Setup, execution and application
testing instructions will be added to the private development repository when its
runnable implementation is available.

## Publication and review

This is a new, current publication of selected materials from development revision
`3c3ff973a237e8d64903643fdf215bb2819ee7b5`, not a reconstructed development history.
The publication branch is `DIP-14-public-materials`. No peer approval is implied.
The reviewed `main` baseline and submission tags in the development repository
remain pending. Existing private PRs have not been merged by this publication.

Public access enables reading and downloading these materials. It does not grant a
software licence or publish the implementation. No open-source licence is granted.
