# Domain docs

## Layout and reading rules

This repository uses a single-context layout:

- `CONTEXT.md` at the repository root contains domain vocabulary.
- `docs/adr/` contains architecture decision records.

Before exploring the codebase, read `CONTEXT.md` and the ADRs
relevant to the area being explored.

If these files do not exist, proceed silently.
The domain-modeling skill creates them when terms or decisions
are resolved.

## Vocabulary

Use the terms defined in `CONTEXT.md` in issue titles,
proposals, hypotheses, and tests.

If a needed concept is missing, reconsider whether it belongs
to the domain or note the gap for domain-modeling.

## Decision conflicts

Explicitly identify proposals that contradict an existing ADR,
reference that ADR, and explain why reopening it is justified.
