# Issue tracker: GitHub

Issues and specs live in GitHub Issues. Use the `gh` CLI.
Infer the repository from the Git remote.

## Operations

- Publish a spec or ticket: `gh issue create --title "..." --body-file <file>`.
- Fetch a ticket and discussion: `gh issue view <number> --comments`.
- Fetch structured details: `gh issue view <number> --json number,title,body,labels,comments`.
- List tickets: `gh issue list --state open --json number,title,body,labels`.
- Comment: `gh issue comment <number> --body-file <file>`.
- Apply or remove labels: `gh issue edit <number> --add-label "..."` or `--remove-label "..."`.
- Close: `gh issue close <number> --comment "..."`.

Write multiline bodies to a temporary file and pass `--body-file`.
Use the label mapping in `triage-labels.md`.

## Pull requests as a triage surface

PRs as a request surface: no.

## Wayfinding operations

- Map: an issue labelled `wayfinder:map`, containing Notes,
  Decisions-so-far, and Fog.
- Child tickets: GitHub sub-issues of the map. If unavailable,
  use a task list in the map and `Part of #<map>` in each child.
- Ticket types: `wayfinder:research`, `wayfinder:prototype`,
  `wayfinder:grilling`, or `wayfinder:task`.
- Blocking: use native GitHub issue dependencies. If unavailable,
  record `Blocked by: #<number>` in the child body.
  A ticket is unblocked when every blocker is closed.
- Frontier: choose the first open, unblocked, unassigned child
  in map order.
- Claim: assign the ticket to the driving developer before work.
- Resolve: comment with the answer, close the ticket, and append
  a summary and link to the map's Decisions-so-far.
