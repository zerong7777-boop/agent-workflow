# Handoffs And Restarts

The restart brief is the main mechanism for recovering long-running work.

## Restart Brief

A restart brief is a compact, edited packet. It should be short enough to paste into a new agent session and complete enough to prevent repeated discovery work.

It should contain:

- task objective;
- current state;
- active constraints;
- key evidence;
- latest decision;
- open loops;
- next action;
- known traps.

## Session Handoff

A session handoff is narrower. It explains what happened inside one execution thread and how to resume from that thread if needed.

## Task Handoff

A task handoff is broader. It should be the default continuation surface for a new session.

## Restart Policy

When context is lost:

1. Start from the task restart brief.
2. Add only the specific session handoff if resuming a known thread.
3. Add evidence records by reference instead of pasting full logs.
4. Ask the agent to restate the next action before making changes.

