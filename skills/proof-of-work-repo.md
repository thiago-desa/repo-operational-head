# Skill: Proof-of-work repo

Use when turning a Grok Bot's work (agent definition, skills, graphs, routines) into a sanitized public GitHub repo, or improving one already published.

## Approval gates

Work autonomously on local, reversible steps. Get the owner's explicit approval before: creating a public repo, the first push, force-pushing or rewriting published history, deleting files or repos, changing visibility, or including anything that might be secret, personal, or private business data.

## Steps

1. **Intake:** read the source bot's profile, its skills, routines, and recent conversation history. Find the proof-of-work story: what it actually does and has done. Never invent capabilities that the source does not show.
2. **Stage** under a workspace repos folder with: README.md, LICENSE (MIT unless told otherwise), .gitignore, ATTRIBUTION.md, agents/ or graphs/, skills/, docs/, examples/ (fictional examples only).
3. **Sanitize:** remove secrets, tokens, `.env` files, emails, phone numbers, addresses, account or agent ids, internal paths, real third-party names when they are personal, and real case, personal, or financial data. Run `skills/sanitize-scan.md` before staging.
4. **Readiness:** README explains what it is and how to use it, no secrets or personal data, LICENSE present, structure navigable, at least one example, attribution present, story obvious to a new reader.
5. **Commit** with a clear message, for example `Add initial public structure for <name> proof-of-work`. Commit as the owner's GitHub noreply identity.
6. **Present** the result with a proposed repo name, description, and topics. Stop for approval.
7. **Once approved,** create the public repo and push, then set description and topics.
8. **Afterwards,** offer launch-post drafts for the owner's review. Never post them without an explicit go-ahead.

## Improving an existing repo

Pull it, compare it against the readiness checklist, propose specific changes, make them, and commit. Normal pushes of small improvements are fine; anything significant or history-rewriting needs approval.

## Portfolio

Keep a short memory of each managed repo, its URL, and how the repos relate. Suggest the next highest-leverage repo or improvement.
