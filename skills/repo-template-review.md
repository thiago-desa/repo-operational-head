# Skill: repo-template-review

Living review protocol for GitHub repositories and Grok Bot / agent templates. Use after staging a proof-of-work repo, before calling it ready, and during recurring portfolio reviews.

## When to use

- A staged repo is about to be marked ready for owner approval.
- An existing public portfolio repo needs a quality pass.
- A Grok Bot template should be scored against the same principles (produce ready-to-apply edits; this skill does not republish another bot's template).

## Core principles

1. **Structure beats scale.** Explicit relationships, schemas, and layered systems beat more context or bigger models. Gaps and contradictions must be visible.
2. **Closed improvement loop.** Extraction, then knowledge base, then grounding, then agent reasoning, then verification, then update. Systems that only answer, or only build a graph, are incomplete. Check measurement, contradiction handling, timestamps, and scheduled maintenance.
3. **Evaluation-driven development.** Every significant claim or change needs a measurable check (deterministic code evals, LLM-as-judge, human in the loop). Evaluate the evals themselves.
4. **Super-agent traits** (for agent templates): continuous context, productive parallel work, proactive event-driven triggers, persistence and recovery. Prefer two-level design (router plus isolated workers), fast-path and semantic trigger filtering, separation of compute / state / environment, a watchdog loop, and plugin modularity.
5. **Context as a budget.** Prefer just-in-time, structured retrieval. Flag context pollution, truncation without summaries, and missing provenance.
6. **Agent-friendly repos.** Short high-signal `AGENTS.md`, clear structure, ADRs where needed, ownership, hard boundaries, atomic commits, and tests as sensors.

## Steps

1. **Ingest.** Read README, layout, `AGENTS.md`, key source files, tests, CI, architecture docs, and any agent / harness / template definitions.
2. **Research.** Look up current best practice (primary, recent sources). Note dates and contradictions; resolve by strength of evidence.
3. **Cross-reference** against the principles and against `graphs/review-graph.md`. Find missing layers (verification, entity resolution, evals, isolation, event filtering, update loop).
4. **Correct.** Rank issues by leverage. Give concrete fixes, reasoning tied to a source, and how to verify each fix. Call out security, permission, and untrusted-input risks.
5. **Update the graph.** Propose new nodes or refinements so future reviews improve.

## Checklist: GitHub repo

- Predictable layout (`agents/` or `src/`, `skills/`, `docs/`, `evals/`, `examples/`, `scripts/`). No misc/temp folders.
- README covers purpose, architecture summary, quickstart, layout, and (for Grok Bot work) an import link.
- `AGENTS.md` is short and high-signal: commands, non-default conventions, hard boundaries, definition of done.
- Architecture docs explain why. ADRs when decisions are non-obvious.
- Tests / linters / hygiene checks run in CI. Small atomic commits.
- No secrets. Clear permission boundaries. Untrusted input handled.
- `LICENSE`, `CONTRIBUTING.md` present (`CODEOWNERS` when a team exists).
- For AI / agent repos: evals or golden sets, observability of agent steps, documented context strategy, modular skills, separation of concerns.

## Checklist: Grok Bot or agent template

- Architecture moves toward super-agent traits where they fit. Isolation for multi-task work. Event triggers with filtering. Clear tool contracts. Context budget respected. Verification layer (cite evidence, flag contradictions, confidence). Watchdog or recovery path. Maintenance path so knowledge compounds.
- Grounding and evals: documented grounding strategy, entity resolution or dedup for structured knowledge, measurable checks with an error-analysis loop, provenance and timestamps on facts.
- Operations: observability, cost/latency awareness, regression checks, permission model, recovery from offline devices or drifted goals, clear human escalation points.
- Usability: concise drop-in instructions, examples that show correct patterns, documented failure modes and troubleshooting.

## Output format

1. Before score (repo checklist / template checklist), rough 0-10 each.
2. Top gaps by leverage (usually three).
3. Concrete fixes applied or proposed (with verification).
4. Proposed graph additions (new nodes / relationships).

## Hard rules while reviewing

- Never use em dashes or en dashes in written output for this portfolio.
- Never invent capabilities the bot or repo does not evidence.
- Never commit secrets or personal data while applying fixes.
- Irreversible git/GitHub actions still require explicit owner approval.
