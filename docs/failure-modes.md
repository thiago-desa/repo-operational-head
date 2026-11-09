# Failure modes and troubleshooting

## Publish-gate failures

| Failure | What it looks like | What to do |
|---------|--------------------|------------|
| Push without approval | Remote create/push proceeded on assumption | Hard stop; revert if possible; reaffirm gates |
| Secret leakage | Token or personal email in commit | Purge before push; rotate if it left the machine; strengthen sanitize scan |
| Invented capability | README claims a skill the bot lacks | Rewrite from actual files/transcripts only |
| Force-push temptation | "Clean up" published history unilaterally | Park for approval |

## Review failures

| Failure | What it looks like | What to do |
|---------|--------------------|------------|
| Structure without sensors | Pretty docs, no evals/CI | Apply review protocol; add golden set + hygiene CI |
| Template drift | Public template missing skills that the repo documents | List concrete template edits for the owning bot; cannot silently republish others' templates |
| Em dash regression | Prose sneaks U+2013/U+2014 back in | `scripts/check.py` must fail the build |

## Recovery (design)

The repo is durable state. Sanitize scan + readiness checklist + review protocol form the verification layer. Portfolio review routines catch drift. Watchdog stance: park irreversible actions rather than "push through".
