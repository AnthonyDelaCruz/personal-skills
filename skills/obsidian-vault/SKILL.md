---
name: obsidian-vault
description: Use when the user mentions Obsidian, "the vault", a note or a daily note, or asks to capture, jot down, write up, append, or find something in ~/Documents/my-remote-vault.
---

# Obsidian Vault

Vault `my-remote-vault` at `~/Documents/my-remote-vault`. Drive it with the `obsidian` CLI — it keeps the live app's index, link graph, and frontmatter correct. Don't read or write the files directly.

**Run every `obsidian` command with `dangerouslyDisableSandbox: true`.** The CLI talks to the running app over localhost; sandboxed, even `obsidian help` fails with a flat `Vault not found.` That's the network sandbox — not a cwd, vault-flag, or config problem. Don't chase it.

## Writing

```bash
obsidian create name="Title" path="Folder" content="..."   # new note
obsidian append file="Title" content="..."                 # add to one
obsidian daily:append content="- ..."                      # today's daily note
obsidian read file="Title"                                 # before editing
```

`file=` resolves by title; `path=` is an exact path. Quote values with spaces; use `\n` for newlines in `content=`.

`obsidian help` lists every command, `obsidian help <command>` its flags.

## Write notes worth re-reading

The point of a note is being readable weeks later. No walls of text.

- Lead with the conclusion, not the background.
- Headings every few paragraphs; lists and tables over prose.
- If a section runs past ~5 lines, split it or cut it.
- Cut hedging and preamble. Keep the specifics — names, paths, numbers, dates.

## Before overwriting

`create ... overwrite` replaces the **entire** file; this CLI has no partial edit. Run `obsidian read` first and build the new content from what comes back — never from your own earlier draft, or you silently destroy anything changed since.
