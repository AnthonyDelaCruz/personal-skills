# personal-skills

Claude Code skills for my own workflow — the ones that encode personal judgment rather than any team's procedure, so they stay portable across work, side projects, and everything else.

## Requirements

- Claude Code
- The `obsidian` CLI and a running Obsidian app — only for the `obsidian-vault` skill

## Setup

Skills in `~/.claude/skills/` load automatically. Clone this repo there:

```bash
git clone git@github.com:AnthonyDelaCruz/personal-skills.git ~/.claude/skills/personal
```

The directory name sets the namespace, so skills are invoked as `personal:<skill>`. Start a new session to pick up changes.

## Skills

| Skill | What it does | Invoke |
|---|---|---|
| `context-handoff` | Closes out a session — pulls the decisions, blockers, and open threads worth keeping before the history is cleared | `/personal:context-handoff` |
| `grill-me` | Interviews you about a plan or decision as a design tree, in rounds, until nothing is silently assumed | `/personal:grill-me` |
| `to-questionnaire` | Turns a decision you can't answer alone into a questionnaire for whoever holds the missing context | `/personal:to-questionnaire` |
| `obsidian-vault` | Reads and writes the Obsidian vault through its CLI, keeping the app's index and link graph correct | automatic |
| `readme-standardise` | Rewrites a repository's README to a standard, concise shape, deriving every fact from the code | automatic |

Skills that take over a whole turn are explicit-only — they run when typed and never fire on their own. Skills that supply context run automatically.

## Adding a skill

One `SKILL.md` per directory under `skills/`, with `name` and `description` frontmatter. Add `disable-model-invocation: true` for anything that should only run when typed.

A skill belongs here only if it names no employer-internal system — no internal hosts, ticket prefixes, private registries, or work repo names. Anything that does belongs in a private plugin instead, which is what keeps this repo publishable and portable.

See [BACKLOG.md](BACKLOG.md) for candidates considered, what was rejected as duplicating an installed plugin, and when the current set gets reviewed.
