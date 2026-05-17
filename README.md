# Agent Workflow

Task-centered memory and evidence-bound execution for long-running AI work.

Agent Workflow is a reusable operating model for working with AI agents over days or weeks without losing context, rigor, or recoverability. It turns agent conversations into task-centered records with durable memory, explicit handoffs, evidence-bound decisions, and restartable execution loops.

Stop managing agents as chats. Manage them as recoverable workflows.

## Why This Exists

Long-running AI work usually fails in predictable ways:

- useful context stays trapped inside chat history;
- a resumed session cannot tell what matters now;
- experiments, claims, and decisions drift apart;
- promising ideas become ungrounded implementation guesses;
- handoffs depend on copying a long transcript instead of a compact restart packet.

Agent Workflow provides a lightweight structure for avoiding those failures. It is not a GUI, agent runner, or project management app. It is the workflow layer that can sit underneath Codex, Claude, ChatGPT, Cursor, local agents, or a custom harness.

## Core Ideas

### 1. Task-First, Not Chat-First

The task is the source of truth. A task records the goal, constraints, unknowns, stages, decisions, experiments, findings, memory, sessions, and handoffs. A chat session is only one execution channel attached to that task.

### 2. Durable Memory

Agent Workflow separates task memory, session memory, restart briefs, and handoffs. That makes a task recoverable even after a model switch, interrupted session, tool crash, or context reset.

### 3. Evidence-Bound Execution

Claims should point to evidence. Experiment records, logs, metrics, artifacts, and verification notes are first-class workflow objects rather than loose comments in a transcript.

### 4. Bottleneck-to-Mechanism Research Loop

For research work, the default loop is:

```text
bottleneck -> mechanism -> structural rewrite -> bounded eval -> promotion gate
```

The loop prevents premature module/loss/feature additions by forcing every candidate method to name the bottleneck, expected mechanism, falsifier, control slice, and promotion gate before scaling.

### 5. Agent-Agnostic Runtime

The workflow does not depend on a specific AI tool. A runtime can be a terminal agent, a GUI-backed agent, a notebook, or a manual execution process. The workflow records what happened and what should happen next.

## Repository Map

```text
BOOTSTRAP.md           Agent-readable bootstrap protocol
AGENT.md               Copy-paste prompt for local coding agents
codex-home.seed/       Clean local workflow home skeleton
docs/
  workflow/           Core workflow model and research loop
  operating-model/    How to run tasks, memory, and handoffs
templates/
  task/               Task and memory templates
  session/            Session and handoff templates
  experiment/         Experiment record template
  finding/            Finding record template
examples/
  minimal-task/       Small public example of the file layout
checklists/           Reusable quality gates
```

## Quick Start

### Use With Your Own Agent

Paste this into Codex, Claude Code, Cursor Agent, Trae, or another local coding agent:

```text
Please bootstrap a clean local agent workflow home from this public repository:

https://github.com/zerong7777-boop/agent-workflow.git

Read BOOTSTRAP.md from that repository and follow it exactly.

Create the workflow home in a new local directory named codex-home unless I specify another target path. Copy only public workflow assets, templates, checklists, docs, examples, and the clean seed structure. Do not copy auth files, tokens, API keys, session logs, raw private transcripts, SQLite databases, cache directories, local indexes, temporary files, machine-specific config, or private project history.

If the target directory already exists, do not overwrite files. First report what would be added, skipped, or conflicted, then ask me before merging.

When finished, report the target directory, files copied, directories created, files skipped, conflicts, and the recommended first task files to create.
```

For a shorter entrypoint, open `AGENT.md`.

### Manual Use

1. Copy `templates/task/task.md` into your own task folder.
2. Fill in the goal, constraints, unknowns, and success criteria.
3. Keep `templates/task/restart-brief.md` updated as the compact restart packet.
4. Record decisions, experiments, and findings as separate evidence-bound files.
5. Before resuming an agent, provide the restart brief plus the current task status instead of a full transcript.

## Suggested Task Layout

```text
tasks/<task-id>/
  task.md
  memory.md
  restart-brief.md
  decisions/
  experiments/
  findings/
  sessions/
```

This repository intentionally keeps the layout simple. Tool-specific repositories can add indexes, GUI state, adapters, and runtime metadata on top.

## What Not To Commit

Do not commit local auth files, private session traces, runtime databases, logs, tokens, or raw transcripts that contain private work. Public examples should be small, synthetic, and scrubbed.

See `.gitignore` for the default exclusion policy.
