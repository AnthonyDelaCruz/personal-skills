---
name: context-handoff
description: Close out a working session so the next one picks up cleanly — extract what survives before the history is cleared.
disable-model-invocation: true
---

# Context Handoff

Most of a session is scaffolding. A little of it is durable, and that little is invisible once the history is gone. This extracts it before that happens.

## 1. Sweep

Go back through the session and pull out only these:

- **Decisions** — what was chosen, and the reason. The reason is the part that gets lost.
- **In flight** — what is half-done, and the exact stopping point. Name files and functions.
- **Blocked** — what failed, what was already tried, what the next thing to try is.
- **Learned** — non-obvious behaviour discovered along the way: a gotcha, an env quirk, a command that only works one way.
- **Stated preferences** — corrections given this session that should hold next time.

## 2. Filter

Drop anything the repo already records: code structure, git history, what a file contains, anything already in a CLAUDE.md. **Durable** means still true next month *and* not derivable from the code.

Convert every relative date to an absolute one — "yesterday" is meaningless in a file read three weeks later.

## 3. Propose, don't write

Show the handoff as a draft, grouped by the categories above. Then ask where each part lands:

| Kind | Usually belongs in |
|---|---|
| Durable facts, preferences | memory — one fact per file |
| Session narrative, open loops | the vault |
| Decisions tied to this code | the repo, beside the code |

Ask. Never assume a destination, and never write before confirmation.

## 4. Write only what was confirmed

Skip anything the user struck. Report what was written and where.

## The failure mode

Dumping the transcript. A handoff that restates the session is the same as not writing one — the next session reads it and still doesn't know what mattered. If it doesn't change what tomorrow does, cut it.
