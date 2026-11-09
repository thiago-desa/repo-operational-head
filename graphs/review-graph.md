# Review graph

Machine-readable sketch of the living review protocol. Nodes are principles or practices. Edges are directed relationships used during portfolio reviews.

## Nodes

| id | label | kind |
|----|-------|------|
| structure | Structure beats scale | principle |
| closed_loop | Closed improvement loop | principle |
| evals | Evaluation-driven development | principle |
| super_agent | Super-agent traits | principle |
| context_budget | Context as a budget | principle |
| agent_repo | Agent-friendly repository practices | principle |
| agents_md | Short high-signal AGENTS.md | practice |
| golden_set | Golden-set / regression evals | practice |
| hygiene_ci | Secrets/PII/em-dash/link CI sensors | practice |
| failure_modes | Documented failure modes | practice |
| verification | Verification layer (evidence, contradictions, confidence) | practice |
| watchdog | Watchdog / recovery loop | practice |
| approval_gates | Human approval for irreversible actions | practice |
| provenance | Provenance and timestamps on facts | practice |
| isolation | Router + isolated workers | practice |
| entity_resolution | Entity resolution / dedup | practice |
| template_parity | Template contents match public repo claims | practice |

## Edges

| from | relation | to |
|------|----------|----|
| structure | improves | verification |
| structure | improves | entity_resolution |
| evals | steers | closed_loop |
| golden_set | implements | evals |
| hygiene_ci | senses | agent_repo |
| agents_md | implements | agent_repo |
| failure_modes | supports | verification |
| watchdog | implements | super_agent |
| isolation | implements | super_agent |
| approval_gates | protects | agent_repo |
| provenance | required_by | verification |
| context_budget | reduces | pollution risk |
| template_parity | required_by | closed_loop |
| verification | feeds | closed_loop |
| closed_loop | compounds | trust |

## Authority sources (credit, not copied text)

- Andrew Ng, AI engineering skills map (evaluation-driven development, grounding, production hygiene)
- Microsoft GraphRAG research and related graph-engineering practice (structure over flat similarity)
- DeepSeek Harness super-agent design discussions (router/worker, triggers, watchdog, plugins)
- 2026 AGENTS.md practice (short, command-first, boundaries, definition of done)

## Update rule

After each significant portfolio review, append new nodes or edges in a dated note under `docs/review-YYYY-MM-DD.md` and fold durable ones back into this file.
