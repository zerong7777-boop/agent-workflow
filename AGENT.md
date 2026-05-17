# Use This Workflow With Your Own Agent

Paste this into Codex, Claude Code, Cursor Agent, Trae, or another local coding agent:

```text
Please bootstrap a clean local agent workflow home from this public repository:

https://github.com/zerong7777-boop/agent-workflow.git

Read BOOTSTRAP.md from that repository and follow it exactly.

Create the workflow home in a new local directory named codex-home unless I specify another target path. Copy only public workflow assets, templates, checklists, docs, examples, and the clean seed structure. Do not copy auth files, tokens, API keys, session logs, raw private transcripts, SQLite databases, cache directories, local indexes, temporary files, machine-specific config, or private project history.

If the target directory already exists, do not overwrite files. First report what would be added, skipped, or conflicted, then ask me before merging.

When finished, report the target directory, files copied, directories created, files skipped, conflicts, and the recommended first task files to create.
```

Optional target path version:

```text
Please bootstrap a clean local agent workflow home from:
https://github.com/zerong7777-boop/agent-workflow.git

Read BOOTSTRAP.md and follow it exactly. Use this target path:
<PUT_YOUR_TARGET_PATH_HERE>

Use create-only behavior. Do not overwrite existing files without asking. Do not copy private runtime state, auth files, tokens, logs, databases, cache, indexes, or local machine config. Report what you created when done.
```
