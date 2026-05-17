# Research Innovation Loop

The research workflow starts from a bottleneck, not from a module idea.

```text
bottleneck -> mechanism -> structural rewrite -> bounded eval -> promotion gate
```

## 1. Bottleneck

Write one sentence that names the structural reason the current approach fails.

Good:

```text
The model treats semantic similarity as geometric solvability, so high-similarity hard cases and low-similarity easy cases need different evidence paths.
```

Weak:

```text
Add matcher features because correspondences are useful.
```

## 2. Mechanism

State the causal or structural behavior that should change if the idea is correct.

Required fields:

- `mechanism_claim`
- `minimal_mechanism`
- `observable_signature`
- `control_signature`
- `falsifier`

If the mechanism has no control signature, it is not ready for implementation.

## 3. Structural Rewrite

Describe how the model, training process, evaluation, or system interface changes.

The rewrite should be more than:

- concatenating another feature;
- adding a scalar weight;
- adding a small adapter without a mechanism;
- adding a loss without a control condition.

## 4. Bounded Eval

Run the smallest evaluation that can falsify the mechanism.

Requirements:

- matched baseline;
- fixed manifest;
- hard slice;
- control slice;
- explicit verdict;
- artifact paths or logs.

## 5. Promotion Gate

Only promote the idea when bounded evidence supports the mechanism and the control slice remains stable.

Allowed statuses:

- `diagnostic-only`
- `blocked`
- `rejected`
- `weak-inconclusive`
- `method-promising`
- `promotion-ready`

