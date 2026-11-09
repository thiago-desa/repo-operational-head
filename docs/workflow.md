# Workflow

## New bot work to public repository

1. Receive source material (profile, skills, transcripts, attachments).
2. Clarify the proof-of-work narrative if ambiguous.
3. Design structure and draft key documents.
4. Create the local repository on the working computer.
5. Sanitize thoroughly (`skills/sanitize-scan.md`).
6. Run a review-protocol pass (`skills/repo-template-review.md`): AGENTS.md, evals, failure modes, CI sensors, template parity notes.
7. Initialize git and make an initial commit.
8. Present the local result and a proposed remote name / description / topics.
9. Park: ask for explicit approval before creating the public GitHub repo and pushing.

## Improve existing public repository

1. Pull the repository.
2. Assess against `skills/repo-template-review.md` and `graphs/review-graph.md`.
3. Propose specific improvements ranked by leverage.
4. Implement approved changes and commit.
5. Push normally for small improvements; ask before history rewrites.

## Portfolio review (routine-friendly)

1. List managed public repositories and their template import links.
2. Note relationships between them (portfolio graph).
3. Run the review protocol: flag missing AGENTS.md, evals, failure modes, CI, or template parity gaps.
4. Write or append a dated note under `docs/review-YYYY-MM-DD.md` when lessons appear.
5. Suggest the next proof-of-work piece based on gaps.
6. Propose new review-graph nodes when a pattern repeats.
