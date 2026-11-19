# Backlog

The rules behind what gets built here. Individual candidates are tracked as [issues](https://github.com/AnthonyDelaCruz/personal-skills/issues) — this file holds only what isn't per-item work.

## Placement rule

Does the skill name an employer-internal system — an internal host, a ticket prefix, a private registry, a work repo name?

- **Yes** → the private team plugin. Not here.
- **No** → this repo, public, even when work is where it gets used daily.

Corollary: skills here are written arena-agnostic and parameterised. They read the repo they are in rather than hardcoding one, so the same skill serves work, side projects, and anything else.

## Active set

| Skill | Species | Invocation |
|---|---|---|
| `obsidian-vault` | context | auto |

Communication preferences live in the global `~/.claude/CLAUDE.md`, not in a skill — it always loads, needs no trigger, and cannot collide with an installed plugin.

## Candidates

Tracked as issues labelled [`candidate`](https://github.com/AnthonyDelaCruz/personal-skills/issues?q=is%3Aissue+label%3Acandidate), each carrying the evidence that raised it.

## Out of scope for this repo

**Local dev stack — run and tear down.** A repeatable multi-service startup dance, re-explained four times. Under the placement rule it names work repos, so it belongs in the private team plugin. Recorded here so it isn't re-proposed, not tracked here because the work can't be done here.

## Rejected — collides with an installed plugin

Planning, systematic debugging, and skill authoring all duplicate `superpowers`. Code-behaviour rules — don't assume, don't overengineer, stay in scope — are already covered by the global `~/.claude/CLAUDE.md`.

Collision avoidance is deliberate: plugins get installed and then narrowed to the few skills actually wanted, so a new skill that overlaps an existing one is a defect, not redundancy. Check what is already installed before opening a candidate issue.

## Review

Scheduled reviews are tracked as issues labelled [`review`](https://github.com/AnthonyDelaCruz/personal-skills/issues?q=is%3Aissue+label%3Areview). None is scheduled; the last was [#4](https://github.com/AnthonyDelaCruz/personal-skills/issues/4), closed 2026-11-19.

Standing prune criterion: anything in the active set not reached for unprompted gets deleted. An unused skill is context cost on every session and a collision risk on the next install.
