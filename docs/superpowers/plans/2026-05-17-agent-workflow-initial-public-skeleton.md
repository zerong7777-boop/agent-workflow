# Agent Workflow Initial Public Skeleton Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Create a clean public repository skeleton for the reusable Agent Workflow operating model.

**Architecture:** Keep the repository tool-agnostic and documentation-first. Separate core concepts, reusable templates, synthetic examples, and publication safety checks so the workflow can later be consumed by GUI or agent-runner implementations.

**Tech Stack:** Markdown, TOML frontmatter, Git.

---

### Task 1: Public Repository Skeleton

**Files:**
- Create: `.gitignore`
- Create: `LICENSE`
- Create: `README.md`

- [ ] **Step 1: Add public ignore rules**

Add `.gitignore` entries for auth files, sessions, SQLite databases, logs, generated indexes, dependencies, and build outputs.

- [ ] **Step 2: Add license**

Add the MIT license already used by the related local harness.

- [ ] **Step 3: Add README positioning**

Write the repository as a task-centered workflow model, not a GUI or agent runner.

### Task 2: Core Workflow Docs

**Files:**
- Create: `docs/workflow/core-model.md`
- Create: `docs/workflow/research-innovation-loop.md`
- Create: `docs/workflow/evidence-bound-execution.md`
- Create: `docs/operating-model/handoffs-and-restarts.md`

- [ ] **Step 1: Document the core record model**

Define task, memory, session, handoff, and evidence records.

- [ ] **Step 2: Document the research innovation loop**

Capture the bottleneck-to-mechanism loop and promotion statuses.

- [ ] **Step 3: Document evidence-bound execution**

Define verification levels and claim discipline.

- [ ] **Step 4: Document restart handoffs**

Explain restart briefs, task handoffs, session handoffs, and restart policy.

### Task 3: Templates And Example

**Files:**
- Create: `templates/task/task.md`
- Create: `templates/task/memory.md`
- Create: `templates/task/restart-brief.md`
- Create: `templates/session/session.md`
- Create: `templates/experiment/experiment.md`
- Create: `templates/finding/finding.md`
- Create: `examples/minimal-task/task.md`
- Create: `examples/minimal-task/restart-brief.md`
- Create: `checklists/public-release.md`

- [ ] **Step 1: Add TOML-frontmatter templates**

Create small records that can be copied into a task folder.

- [ ] **Step 2: Add a synthetic example**

Add a minimal task and restart brief without private data.

- [ ] **Step 3: Add public release checklist**

List private data and environment artifacts that must not be committed.

### Task 4: Git Preparation

**Files:**
- Modify: local Git metadata only.

- [ ] **Step 1: Initialize Git**

Run `git init -b main`.

- [ ] **Step 2: Review status**

Run `git status --short` and verify only public workflow files are staged later.

- [ ] **Step 3: Set remote**

Run `git remote add origin https://github.com/zerong7777-boop/agent-workflow.git`.

- [ ] **Step 4: Commit**

Run `git add .` and `git commit -m "docs: add initial agent workflow skeleton"`.

- [ ] **Step 5: Push when network and credentials are available**

Run `git push -u origin main`.

