---
title: Tasks
nav_order: 4
parent: How this repo is kept
---

# Tasks

Written by `charter adopt` from the repo's mise tasks (`charter docs-tasks`): don't edit, change the tasks, then `charter adopt`.

Run one with `mise run <task>`; its arguments and flags go after `--`. `mise tasks` lists them, and `mise run <task> --help` shows one.

## From `joeblew999/charter//tasks/repo`

| Task | What it does |
|---|---|
| [`adopt`](#adopt) | Write charter's kit into this repo as this release has it: docs/charter/, the docs site's files, the issue forms, the workflows, AGENTS.md, CLAUDE.md, renovate.json; never a file of the repo's own |
| [`docs:setup`](#docssetup) | Write charter's kit (charter adopt), then the pages docs/_generated.toml lists |
| [`docs:lint`](#docslint) | Check docs/ for what a program can check: front matter, links, the index, tasks and paths that don't exist |
| [`docs:check`](#docscheck) | Fail if a file of charter's kit or a generated page differs from what docs:setup writes, or docs/ fails the lint |
| [`docs:review`](#docsreview) | Have Claude (the claude command) bring docs/ up to date and into line with docs/charter/writing.md |
| [`docs:pages`](#docspages) | REMOTE, once per repo: turn on GitHub Pages for docs/ on main (GitHub renders the markdown itself) |
| [`release`](#release) | REMOTE: cut a release from this machine: mise run release \-\- vX.Y.Z [-dry-run]. The repo is clean and is the default branch on GitHub, then the repo's own tasks where it has them: setup, check, dist. Then the tag, the push, the GitHub Release with notes from the commits. It does not wait for GitHub's workflows: check is the same check, run here; a workflow that FAILED on this commit stops it |
| [`repo`](#repo) | REMOTE: keep the repo on GitHub in shape from charter.toml at its root: labels, description, homepage, topics, GitHub Pages. It writes no file: mise run adopt writes the kit |
| [`repo:check`](#repocheck) | REMOTE, read-only: fail if the repo on GitHub differs from charter.toml (charter repo -check) |
| [`issues`](#issues) | REMOTE, read-only: the open issues, newest first: what is reported and what is planned (a plan is an issue) |
| [`repo:ci`](#repoci) | Everything the charter workflow runs (charter.yml, which calls charter's repo-check), here: docs:check (the docs site and generated pages are fresh, docs/ passes the lint), repo:check (the repo is as charter.toml says), upstream:status. The workflow runs this one task and nothing else, so a pass here is a pass on GitHub. REMOTE, read-only |
| [`issue`](#issue) | Print the body to fill in for an issue of one kind, with that form's headings, and the gh command that files it with the form's labels: mise run issue \-\- bug (or feature, upstream, plan) |
| [`upstream:status`](#upstreamstatus) | REMOTE, read-only: the upstream issues the code works around (every `Upstream:` tag): CLOSED means that workaround can go |

## Each task

### `adopt`

- **Usage:** `adopt`

Write charter's kit into this repo as this release has it: docs/charter/, the docs site's files, the issue forms, the workflows, AGENTS.md, CLAUDE.md, renovate.json; never a file of the repo's own

### `docs:setup`

- **Usage:** `docs:setup`

Write charter's kit (charter adopt), then the pages docs/_generated.toml lists

### `docs:lint`

- **Usage:** `docs:lint`

Check docs/ for what a program can check: front matter, links, the index, tasks and paths that don't exist

### `docs:check`

- **Usage:** `docs:check`

Fail if a file of charter's kit or a generated page differs from what docs:setup writes, or docs/ fails the lint

### `docs:review`

- **Usage:** `docs:review`

Have Claude (the claude command) bring docs/ up to date and into line with docs/charter/writing.md

### `docs:pages`

- **Usage:** `docs:pages`

REMOTE, once per repo: turn on GitHub Pages for docs/ on main (GitHub renders the markdown itself)

### `release`

- **Usage:** `release`

REMOTE: cut a release from this machine: mise run release -- vX.Y.Z [-dry-run]. The repo is clean and is the default branch on GitHub, then the repo's own tasks where it has them: setup, check, dist. Then the tag, the push, the GitHub Release with notes from the commits. It does not wait for GitHub's workflows: check is the same check, run here; a workflow that FAILED on this commit stops it

### `repo`

- **Usage:** `repo`

REMOTE: keep the repo on GitHub in shape from charter.toml at its root: labels, description, homepage, topics, GitHub Pages. It writes no file: mise run adopt writes the kit

### `repo:check`

- **Usage:** `repo:check`

REMOTE, read-only: fail if the repo on GitHub differs from charter.toml (charter repo -check)

### `issues`

- **Usage:** `issues`

REMOTE, read-only: the open issues, newest first: what is reported and what is planned (a plan is an issue)

### `repo:ci`

- **Usage:** `repo:ci`

Everything the charter workflow runs (charter.yml, which calls charter's repo-check), here: docs:check (the docs site and generated pages are fresh, docs/ passes the lint), repo:check (the repo is as charter.toml says), upstream:status. The workflow runs this one task and nothing else, so a pass here is a pass on GitHub. REMOTE, read-only

### `issue`

- **Usage:** `issue`

Print the body to fill in for an issue of one kind, with that form's headings, and the gh command that files it with the form's labels: mise run issue -- bug (or feature, upstream, plan)

### `upstream:status`

- **Usage:** `upstream:status`

REMOTE, read-only: the upstream issues the code works around (every `Upstream:` tag): CLOSED means that workaround can go
