# AGENTS.md

Short, high-signal instructions for coding agents working in `repo-operational-head`.

## What this repo is

GitHub / Repo Operational Head: sanitize Grok Bot work into MIT public repos, park irreversible git steps for approval, and review portfolios against a living protocol.

This is a sanitized proof-of-work snapshot of a Grok Bot design. Markdown skills and docs are the product. There is no service binary to compile.

## Layout

| Path | Role |
|------|------|
| `agents/` | Sanitized agent definition |
| `skills/` | Proof-of-work staging, sanitize scan, getting started, repo-template review |
| `graphs/` | Portfolio schema and review-graph principles |
| `docs/` | Architecture, workflow, failure modes, dated review findings |
| `evals/` | Golden set for staging and review gates |
| `examples/` | Fictional stage-and-park walkthrough |
| `scripts/check.py` | Hygiene CI entrypoint |

## Commands

```bash
python scripts/check.py
```

Local staging happens under a workspace repos folder on the bot's computer. Never push or create a public repo without an explicit owner yes.

## Hard boundaries

- Never commit secrets, tokens, passwords, private keys, or `.env` files.
- Never publish real personal data, private business facts, or live case material.
- Approval required for: creating a public repo, first push, force-push, delete, visibility change, or anything that might contain secrets.
- Default license MIT unless the owner says otherwise.
- No em dashes or en dashes in prose.
- Never invent capabilities the source bot does not show.

## Definition of done

- Readiness checklist in `skills/proof-of-work-repo.md` satisfied.
- Sanitize scan clean.
- Review protocol considered for agent repos (`skills/repo-template-review.md`).
- `python scripts/check.py` passes.
- Irreversible steps still parked unless the owner already approved the exact action.
- README import link intact.

## Ownership

Maintained by Thiago De Sa. Irreversible git/GitHub actions (new public repo, first push, force-push, delete, visibility change) need the owner's explicit approval even when an agent stages the work.
