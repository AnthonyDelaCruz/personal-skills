# Investigation template

Something was tracked down. The note answers two things: **what happened**, and **is any action ours**.

## Frontmatter

```yaml
---
tags: [investigation, <subject>, <system if there is one>]
---
```

## Skeleton

```markdown
Investigated <YYYY-MM-DD>. <What was reported, by whom, and the symptom.>

## Conclusion

<The verdict, three sentences at most.>

<Who owns the fix. "Not ours" is common and valid — say it plainly, and say whose it is.>

## What actually happens

The mechanism as a numbered list, one step per hop. Mark the step that fails.

## Evidence

Tables. Numbers, dates, IDs, file paths with line numbers. The conclusion must be
re-derivable from this section alone.

## Not established

What could not be confirmed, and what confirming it would take.

## Action items

- **Ours:** the cheap changes, in domains under our control.
- **Not ours:** who to raise it with, and the exact ask.
```

## Rules

- **Conclusion first.** Never open with background.
- **Three sentences** for the verdict. Any section past ~5 lines splits or gets cut. Tables over prose.
- **Keep the specifics** — names, paths with line numbers, IDs, counts, dates. Convert every relative date to an absolute one.
- **Never omit `Not established`.** An unmarked gap reads as a finding.
- **Unresolved items are recorded, never chased.** Don't offer to go verify them; each is a candidate for its own debrief.
- **Never guess the owner.** If you can't tell, it's an unresolved item.

## Diagram

A fenced `mermaid` block, linked from the mechanism section. It never replaces the numbered mechanism: the diagram carries the topology, the list carries the endpoints and line numbers.

- `sequenceDiagram` for a request hopping across systems. `flowchart` for components or conditions. `stateDiagram-v2` only for genuine states. Nothing else.
- **No `style` or `classDef`** — hardcoded colours break one of the two Obsidian themes.
- Label edges with the real endpoint or status, not "calls". Quote any label containing punctuation: `A["GET /x (cached)"]`.
- Past ~10 nodes, the mechanism wants its own sub-notes instead.
