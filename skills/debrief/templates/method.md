# Method template

How to redo this yourself next time. The investigation note says what was wrong; this one says how to find it again without help.

## Frontmatter

```yaml
---
tags: [method, <subject>, <system>]
---
```

## Skeleton

```markdown
Written up from the <Topic> investigation on <YYYY-MM-DD>. Links back: [[<Topic>]]

## 1. <Pick the right starting point>

The choice that wastes the most time if you get it wrong — which instance, which repo,
which environment. A table of the options and how to tell them apart.

## 2. <What to know before searching>

The two or three facts that make the queries below make sense.

## 3. The query that matters

The one command that usually answers the question, verbatim in a fenced block.

## 4. <Following it further>

The steps for the harder case, in order. Each with its command and what its output looks like.

## Gotchas

The wrong turns. What looks right and isn't, and how to tell.
```

## Rules

- **Commands verbatim, in fenced blocks.** A paraphrased command is useless.
- **Show what the output looks like** — a trimmed real example beneath each command, so a wrong result is recognisable.
- **Order by what wastes the most time.** The choice that sends you to the wrong place entirely comes first.
- **Gotchas earn their own section.** They're the reason this note exists rather than the docs.
- **Written to be run without an agent.** Nothing may depend on context only this conversation had.
- Link back to the investigation it came from, and have that note link here.
