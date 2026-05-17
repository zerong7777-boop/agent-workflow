# Local Agent Workflow Home

This directory is a clean local workflow home created from `agent-workflow`.

Use it to keep long-running AI agent work recoverable:

- `templates/` contains reusable task, memory, experiment, finding, and session records.
- `checklists/` contains quality gates before publishing or sharing work.
- `docs/` contains the workflow operating model.
- `tasks/` contains active task folders.
- `memory/` contains durable local memory that is safe to keep on this machine.
- `restart-briefs/` contains compact packets for resuming interrupted work.
- `artifacts/` contains generated outputs, logs, reports, and verification evidence.

Do not store tokens, API keys, auth files, private transcripts, raw session logs, or local databases in public Git history.
