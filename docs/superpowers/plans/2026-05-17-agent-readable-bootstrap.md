# Agent-Readable Bootstrap Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Add an agent-readable bootstrap protocol so users can paste one prompt into Codex, Claude Code, Cursor Agent, Trae, or another local agent and recreate a clean workflow home from this repository.

**Architecture:** The repository remains the public source of workflow assets. `BOOTSTRAP.md` is the executable instruction document for agents, `AGENT.md` is the human-facing copy-paste entrypoint, and `codex-home.seed/` is a minimal clean target skeleton. Agents copy public assets into a user-selected local directory without copying private runtime state.

**Tech Stack:** Markdown instructions, repository file layout, Git verification.

---

### Task 1: Add Bootstrap Protocol

**Files:**
- Create: `BOOTSTRAP.md`
- Create: `AGENT.md`

- [x] **Step 1: Define the agent execution protocol**

Create `BOOTSTRAP.md` with the goal, target directory rules, copy rules, safety policy, and completion report format.

- [x] **Step 2: Define the user copy-paste prompt**

Create `AGENT.md` with one concise prompt that users can paste into their own local coding agent.

### Task 2: Add Clean Workflow Home Seed

**Files:**
- Create: `codex-home.seed/README.md`
- Create: `codex-home.seed/.gitignore`
- Create: `codex-home.seed/tasks/README.md`
- Create: `codex-home.seed/memory/README.md`
- Create: `codex-home.seed/restart-briefs/README.md`
- Create: `codex-home.seed/artifacts/README.md`

- [x] **Step 1: Create the seed directory**

Add a minimal seed structure that is safe to copy into a new local workflow home.

- [x] **Step 2: Add local privacy defaults**

Add a seed `.gitignore` that excludes auth files, session traces, logs, databases, cache, and private memory.

### Task 3: Document Usage

**Files:**
- Modify: `README.md`

- [x] **Step 1: Update repository map**

Add `BOOTSTRAP.md`, `AGENT.md`, and `codex-home.seed/` to the repository map.

- [x] **Step 2: Add one-prompt bootstrap instructions**

Add a section showing how to paste a single instruction into a local agent.

### Task 4: Verify and Publish

**Files:**
- Verify: all changed files

- [ ] **Step 1: Search for conflict markers**

Run: `rg -n "\<{7}|={7}|\>{7}" .`

Expected: no matches.

- [ ] **Step 2: Check Git status**

Run: `git status -sb`

Expected: only intended files are modified or added.

- [ ] **Step 3: Commit and push**

Run:

```powershell
git add BOOTSTRAP.md AGENT.md codex-home.seed README.md docs/superpowers/plans/2026-05-17-agent-readable-bootstrap.md
git commit -m "docs: add agent-readable bootstrap"
git push
```

Expected: remote `main` updates successfully.
