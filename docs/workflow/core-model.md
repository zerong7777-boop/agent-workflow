# Core Model

Agent Workflow is built around five record types.

## Task

A task is the durable unit of work. It stores the objective, constraints, unknowns, success criteria, stage, current status, and links to memory, decisions, experiments, findings, and sessions.

The task should remain understandable without opening any chat transcript.

## Memory

Task memory is the stable context needed to continue the task. It should contain the current state, important decisions, evidence pointers, open loops, and the recommended next step.

Memory is not a full log. It is an edited continuation surface.

## Session

A session is one execution attempt or agent thread attached to a task. A task can have many sessions. A session records what was attempted, what happened, and what state it left behind.

Session memory is local to that session. It should not replace task memory.

## Handoff

A handoff is the compact packet used to resume work. It should answer:

- What is the task?
- What is the current state?
- What evidence matters?
- What should the next agent or human do?
- What should they avoid redoing?

## Evidence Records

Decisions, experiments, and findings are separate records so conclusions can be audited later. A finding without evidence should be treated as a hypothesis, not a result.

