# Skill: Sanitize scan

Run before every commit to a proof-of-work repo.

## Grep targets (fix or remove hits)

- Tokens and keys: `sk-`, `ghp_`, `gho_`, `xox`, `Bearer `, `BEGIN PRIVATE KEY`, `.pem`
- Env and vault: `.env`, `vault_`, `VAULT`, `password`, `api_key`, `secret`
- Contact and identity: email-shaped strings, phone patterns, street addresses
- Internal ids: long hex agent ids, `serverId`, machine hostnames like `DESKTOP-`
- Absolute private paths that name a real user home
- Em dash characters when the owner forbids them
- Real case, financial, or medical details

## Rules

- Fictional examples only in `examples/`.
- Public contact seeds must come from official public pages and be labeled as such.
- If unsure whether a string is personal, leave it out and ask.
