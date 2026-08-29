---
name: readme-standardise
description: Rewrite a repository's README to a standard, concise shape. Use when the user asks to standardise, clean up, or write a README for any repo.
---

# README Standardise

A README is a landing page, not a manual. Someone who has never seen the repo should be running it in five minutes; everything deeper is a link.

## Derive every fact from the code

Read the manifest — `package.json`, `pom.xml`, `Cargo.toml`, `go.mod`, `Makefile`, compose files — and take the real scripts, versions, and ports from it.

Never copy facts from the existing README, a CLAUDE.md, or a wiki. Those drift; the manifest doesn't. If the old README disagrees with the code, the code is right and the README was stale — that is the reason for the rewrite.

## The shape

```markdown
# <repo name>

One sentence: what this is and who it is for.

## Requirements

Runtime and language versions, plus external services it needs. Versions only —
never how to install them.

## Setup

The steps from clone to a working checkout. Real commands, taken from the manifest.

## Running

How to start it, and what you get when it works — a URL, a port, a log line.

## Testing

How to run the tests.

## Layout

Only when the structure isn't self-evident. A short table of the directories that matter.

## Configuration

Environment variables that must be set and what each does. Never real values.
```

## Rules

- **No runtime-manager instructions.** State that it needs Node 18 or Java 21; don't tell anyone to use `mise`, `nvm`, `asdf`, or `pyenv`. Other people have their own.
- **Nothing machine-specific.** No `/Users/<name>/…`, no usernames, no local ports that only work on one setup.
- **Delete empty sections.** Never `N/A`, never `TBD`, never a heading with nothing under it.
- **Same standard everywhere.** No per-repo exceptions — a standard with exceptions isn't one.
- **Link out for depth.** Architecture, runbooks, and troubleshooting live in their own docs and get one line here.

## Before writing

Show the draft and confirm before overwriting an existing README — it may carry a badge, a licence note, or a section that isn't derivable from the code and shouldn't be lost.
