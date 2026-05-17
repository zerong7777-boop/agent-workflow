# Agent Workflow Bootstrap

This document is written for local coding agents. Follow it to create a clean local workflow home from this repository.

## Goal

Create a reusable local workflow directory for long-running AI agent work. The result should be a clean workspace for task records, durable memory, restart briefs, checklists, and evidence-bound execution notes.

## Source Repository

Use this repository as the source:

```text
https://github.com/zerong7777-boop/agent-workflow.git
```

If the repository is not already available locally, clone it to a temporary or user-approved location before reading files.

## Default Target

If the user does not specify a target path, create a new directory named `codex-home` under the user's current working directory.

If a directory named `codex-home` already exists, do not overwrite it. Report that it exists and ask the user for a different target path or permission to merge missing files.

## Required Inputs

Use these defaults unless the user gives different instructions:

```text
target: ./codex-home
mode: create-only
overwrite: false
```

## Copy Rules

Copy these public workflow assets into the target directory:

```text
templates/
checklists/
docs/workflow/
docs/operating-model/
examples/
codex-home.seed/
```

When copying `codex-home.seed/`, copy its contents into the root of the target directory. Do not create a nested `codex-home.seed` folder inside the target.

The target should contain this shape when finished:

```text
codex-home/
  README.md
  .gitignore
  templates/
  checklists/
  docs/
    workflow/
    operating-model/
  examples/
  tasks/
  memory/
  restart-briefs/
  artifacts/
```

## Create Empty Local Directories

Create these directories if they do not already exist:

```text
tasks/
memory/
restart-briefs/
artifacts/
```

Keep the `README.md` files inside these directories when they come from the seed. They explain the purpose of each local area and keep empty directories visible in Git.

## Never Copy

Do not copy private or machine-specific state. Exclude:

```text
auth files
API keys
tokens
session logs
raw private transcripts
SQLite databases
cache directories
local indexes
temporary files
machine-specific config
private project history
```

Also exclude files or directories matching:

```text
auth.json
history.jsonl
*.sqlite
*.db
*.log
*.local.*
.env
.env.*
sessions/
cache/
tmp/
indexes/
memories/private/
.codex/
.sandbox/
.sandbox-secrets/
```

## Safety Policy

Use create-only behavior by default.

If the target directory already exists:

1. Inspect the target.
2. Report which files would be added.
3. Report which files already exist.
4. Do not overwrite existing files unless the user explicitly approves.

If a source file and target file differ, keep the target file unchanged and report the conflict.

## Completion Report

After bootstrapping, report:

```text
target directory:
files copied:
directories created:
files skipped:
conflicts:
recommended first task file:
```

Recommend starting with:

```text
tasks/<task-id>/task.md
tasks/<task-id>/memory.md
tasks/<task-id>/restart-brief.md
```

The user can create these from:

```text
templates/task/task.md
templates/task/memory.md
templates/task/restart-brief.md
```

## Success Criteria

The bootstrap is complete when:

- the target directory exists;
- public workflow assets are copied;
- local task, memory, restart brief, and artifact directories exist;
- no private runtime state was copied;
- existing user files were not overwritten without approval;
- the user receives a clear completion report.
