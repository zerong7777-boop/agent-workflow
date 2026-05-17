# Evidence-Bound Execution

Agent Workflow treats evidence as part of the work product.

## Rule

Do not let a conclusion stand alone. Link it to the record that supports it.

Examples:

- A decision links to the tradeoff and selected option.
- An experiment links to config, code snapshot, command, metric, and artifact.
- A finding links to the experiment or source that justifies it.
- A handoff links to the current task memory and recent evidence.

## Verification Levels

Use the smallest level that answers the current question.

```text
config parse -> smoke run -> bounded eval -> full run -> promotion review
```

## Claim Discipline

Smoke runs can prove that mechanics work. They cannot prove that a method works.

Bounded evals can support or reject a mechanism under specific conditions.

Full runs can support broader claims only when the baseline, split, checkpoint, and metric provenance are clean.

