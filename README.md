# repo-operational-head

GitHub / Repo Operational Head Grok Bot: turns Grok Bot works (graphs, skills, routines, agent definitions, playbooks) into clean, sanitized, well-documented public GitHub repositories as proof of work, and keeps the portfolio improving.

## Problem it solves

Private bot work is hard to show. This design takes real agent definitions and skills, strips secrets and personal data, stages a navigable MIT-licensed repo, and parks irreversible steps (create public repo, first push, force-push, delete, visibility change) for explicit owner approval.

## How to use with Grok Bot

1. Create a new Grok Bot (suggested name: `repo · Repo Operational Head`).
2. Paste the contents of `agents/repo-operational-head.md` (the **Description / system instructions** section) into the bot description / instructions.
3. Keep the skills in `skills/` alongside the bot.
4. Confirm the preferred GitHub username or organization and that MIT is the default license.
5. Point it at the first bot or body of work to publish. It will stage locally under a workspace repos folder and stop before any public create or push.

## Import into Grok Bot

[Import Repo Operational Head](https://x.ai/bot/QmoolLJGIjtCLyVe0m9Ii)


## Key files

| Path | What it is |
|------|------------|
| `agents/repo-operational-head.md` | Full sanitized agent definition |
| `graphs/portfolio-schema.md` | Portfolio entities and relationships |
| `skills/proof-of-work-repo.md` | End-to-end staging and publish gates |
| `skills/sanitize-scan.md` | Secrets and PII grep checklist |
| `skills/repo-head-getting-started.md` | First-conversation setup |
| `docs/architecture.md` | Super-agent style operating model |
| `docs/workflow.md` | Intake through approval gates |
| `examples/fictional-stage-and-park.md` | Fully fictional staging walkthrough |
| `ATTRIBUTION.md` | Design influences |
| `LICENSE` | MIT |
| `AGENTS.md` | Short agent instructions, boundaries, definition of done |
| `CONTRIBUTING.md` | How to propose changes safely |
| `docs/failure-modes.md` | Failure modes and troubleshooting |
| `evals/` | Golden-set behavioral regressions |
| `scripts/check.py` | Secrets/PII/em-dash/link hygiene checks |
| `scripts/github-workflow-checks.yml` | GitHub Actions workflow (copy to `.github/workflows/checks.yml` when the token has `workflow` scope) |
| `skills/repo-template-review.md` | Living review protocol for repos and templates |
| `graphs/review-graph.md` | Principles and relationships used in reviews |
| `docs/review-2026-11-09.md` | Review findings and lessons (2026-11-09) |

## Proof-of-work notes

This repository is a cleaned public snapshot of the Repo Operational Head role itself:

- Standard public repo template (README, MIT LICENSE, .gitignore, ATTRIBUTION, agents/, skills/, docs/, examples/)
- Explicit approval gates for irreversible git and GitHub actions
- Sanitize-before-stage discipline
- Portfolio graph of bots, skills, and repositories

## Review findings

Portfolio review notes (repos and templates): [docs/review-2026-11-09.md](docs/review-2026-11-09.md).

## License and attribution

MIT License. Copyright (c) 2026 Thiago De Sa.

Design influences are listed in `ATTRIBUTION.md`.
