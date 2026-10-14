---
# Started by `charter adopt` (github.com/joeblew999/charter): yours to edit.
title: Start here
nav_order: 1
permalink: /
---

# charter-adopt-test

Everything written about this repo lives in this folder. `AGENTS.md` only points here.

| Page | What it covers |
|---|---|
| This page | What is what |
| [rules.md](rules.md) | This repo's own rules |
| [charter/](charter/README.md) | Charter's part, the same in every repo it keeps: [the rules they share](charter/rules.md), [using charter](charter/using.md), [writing docs](charter/writing.md), [the tasks](charter/tasks.md) |

## What is what

Say here what this repo is, and where its parts are: a row per part.

| Name | Where | What it is |
|---|---|---|
| The tasks | `mise.toml` | [Tasks](charter/tasks.md) lists them, written from the tasks themselves; those any repo takes come from [charter](https://joeblew999.github.io/charter/guides/any-repo.html) |

## What is generated

Never edit these: change the source and run the task.

| Path | Written by |
|---|---|
| `docs/charter/`, and the docs site's `_config.yml`, `llms.txt` and `_sass/` | `mise run docs:setup` |
| A page that `_generated.toml` in `docs/` lists | `mise run docs:setup`, from its command |
| `.github/ISSUE_TEMPLATE/charter-*.yml`, `config.yml`, `.github/workflows/charter.yml`, `renovate.json`, `AGENTS.md`, `CLAUDE.md` | `mise run repo` |
