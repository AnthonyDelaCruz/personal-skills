# Backlog

Skill candidates considered and parked, with the evidence that raised them. Reviewed alongside the active set — see **Review** below.

## Placement rule

Does the skill name an employer-internal system — an internal host, a ticket prefix, a private registry, a work repo name?

- **Yes** → the private team plugin. Not here.
- **No** → this repo, public, even when work is where it gets used daily.

Corollary: skills here are written arena-agnostic and parameterised. They read the repo they are in rather than hardcoding one, so the same skill serves work, side projects, and anything else.

## Active set

| Skill | Species | Invocation |
|---|---|---|
| `context-handoff` | process | explicit only |
| `readme-standardise` | procedure | auto |

Communication preferences live in the global `~/.claude/CLAUDE.md`, not in a skill — it always loads, needs no trigger, and cannot collide with an installed plugin.

## Parked

**Pedagogy — explaining unfamiliar code at beginner level.** The largest arena-agnostic pattern found: 123 "explain / walk me through" prompts across 14 projects, plus 17 separate requests to explain at beginner level. Dropped only because it arrived bundled with the learning arena. The strongest candidate for the next batch.

**Local dev stack — run and tear down.** A repeatable multi-service startup dance re-explained four times. Names work repos, so under the placement rule it belongs in the private team plugin, not here. Separate errand.

**Vault hygiene.** Three separate requests amounting to "total re-vamp, it got unwieldy real quick". Recurring, but the shape of the fix isn't settled — unclear whether it is a skill or a one-off reorganisation.

**Screenshot-driven prompts.** 85 occurrences across 10 projects where a pasted image is the entire prompt. Real pattern; no clear skill shape yet.

## Rejected — collides with an installed plugin

Planning, systematic debugging, and skill authoring all duplicate `superpowers`. Code-behaviour rules — don't assume, don't overengineer, stay in scope — are already covered by `karpathy-guidelines`. Collision avoidance is deliberate: plugins get installed and then narrowed to the few skills actually wanted, so a new skill that overlaps an existing one is a defect, not redundancy.

## Review

**2026-09-12**, after two weeks of real use.

Prune criterion: anything in the active set not reached for unprompted gets deleted. An unused skill is context cost on every session and a collision risk on the next install.
