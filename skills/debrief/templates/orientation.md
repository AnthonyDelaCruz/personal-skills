# Orientation template

A topic was explained. The note is a concise, high-level version — enough to hold the shape in your head and ask better follow-up questions.

Not a tutorial and not a reference. If it starts covering everything, it's the wrong template.

## Frontmatter

```yaml
---
tags: [orientation, <subject>, <system if there is one>]
---
```

## Skeleton

```markdown
Looked into <YYYY-MM-DD>. <What this is and why it came up.>

## What it is

Two sentences. No history, no background.

## How it hangs together

The mechanism as a numbered list. The moving parts and what passes between them.

## Vocabulary

| Term | What it actually means |

Terms that would otherwise have to be inferred from context.

## Where to look

Entry points with real paths — the files, dashboards or commands to start from.

## What I still don't get

Named openly, never quietly omitted. These are the follow-up questions worth asking.
```

## Rules

- **Beginner level by default.** Name the concept, give the analogy, then show the code or command. Assume no prior knowledge of the language, tool, or framework.
- **Any section past ~5 lines splits or gets cut.** Tables over prose.
- **Real names, not placeholders.** A generic explanation is worthless a month later.
- **`What I still don't get` is not optional.** It's the most useful section — it's the list of what to ask next.

## Diagram

`flowchart LR` of the components and what flows between them, linked from `How it hangs together`.

No `style` or `classDef` — hardcoded colours break one of the two Obsidian themes. Quote labels containing punctuation.
