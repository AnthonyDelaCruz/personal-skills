---
name: debrief
description: Write up the conversation that just happened as vault notes you can actually learn from.
disable-model-invocation: true
---

# Debrief

Turn the conversation that just happened into a concise, understandable write-up in the vault. It's a learning tool: the point is understanding the whole thing without reading a wall of text. The conversation already did the work — never re-run it.

## 1. Ask two things, in one exchange

Before writing anything, put both choices to the user.

**Template** — then read only the one picked.

| Template      | Use it for                                                                                                                                             | Read                         |
| ------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------ | ---------------------------- |
| Investigation | tracking something down — failure logs, a cross-team issue, why one thing behaves unlike its siblings. Ends in: what happened, and is any action ours? | `templates/investigation.md` |
| Orientation   | learning a topic in general. Concise, high-level, enough to ask better follow-up questions.                                                            | `templates/orientation.md`   |
| Method        | how to redo it yourself next time — the steps, the commands, the wrong turns.                                                                          | `templates/method.md`        |

**Area** — `Work` or `Learning`.

## 2. Write the main note

One folder per topic, even when it holds a single note.

| Template      | Folder                           |
| ------------- | -------------------------------- |
| Investigation | `<Area>/Investigations/<Topic>/` |
| Orientation   | `<Area>/Orientation/<Topic>/`    |

```
<folder>/
  <Topic>.md            ← always; the index
  <Topic> — Flow.md     ← a diagram, once one is wanted
  <Topic> — Method.md   ← how to redo it, once one is wanted
  <Sub-area>.md         ← one per area that needs its own depth
```

Write the index, report its path, and stop there.

## 3. Then offer the extras

Once the user has read the index, ask whether they want either. Never write one unasked.

- **A Method note** — only when the path would otherwise be rediscovered from scratch: which of several near-identical instances, which repos in which order, which query.
- **A diagram** — only when the shape is the hard part. The picked template says how to draw it.

## Rules

- Filenames carry the topic, so `file="<Topic>"` resolves and `[[<Topic>]]` stays unambiguous across folders.
- The index holds the spine. Every other note in the folder links back to it; the index links out to each.
- A topic already in the vault as a flat note gets `obsidian move file="<Topic>" to="<folder>"` first — moving through the app rewrites the wikilinks pointing at it.
- All vault writes go through the `obsidian-vault` skill.
