# Portfolio schema

Lightweight graph for the collection of managed proof-of-work repositories.

## Entities

| Type | Meaning |
|------|---------|
| Bot | A Grok Bot whose work is being published |
| Graph | A typed knowledge or operating graph |
| Skill | A reusable narrow playbook |
| Routine | A scheduled automation |
| Repository | A staged or public GitHub repo |
| ProofArtifact | README, example, script, or other public evidence |
| Example | A fictional walkthrough |

## Relationships

| Edge | From -> To |
|------|------------|
| implements | Repository -> Bot |
| depends_on | Skill -> Skill / Graph |
| demonstrates | Example -> Skill / Bot |
| improves_upon | Repository -> Repository |
| sources_from | Repository -> Bot / Graph / Skill |

## Rules

- Prefer explicit structure over dumping raw transcript text.
- Public nodes never store secrets, personal data, or internal ids.
