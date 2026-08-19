# DPP Benchmarks

DPP benchmarks compare the same task under matched conditions:

- **Control:** the model receives the task without DPP.
- **DPP:** the same model receives the same task after the frozen DPP Operational Edition.

Results are evidence, not advertising. Wins, ties, losses, regressions, mistakes, and inconclusive outcomes must be preserved.

## Benchmark status

| Benchmark | Task | DPP version | Status |
|---|---|---|---|
| [001](results/benchmark-001/RESULTS.md) | SafeKeep launch package | v1.3 | Complete — Control 35/40; DPP 37.5/40 |
| [002](benchmarks/benchmark-002/TASK.md) | Production Rescue | [v1.4](operational/DPP-v1.4-Operational.md) | Frozen; execution pending |
| 003 | Independent paired test | Current version at freeze | Reserved for an independent participant |

Benchmark 001 is one observed result, not proof that DPP improves every model or task. Benchmark 002 is a separate production-code repair benchmark and does not replace or revise Benchmark 001.

## Matched-run method

1. Freeze the task, scoring rubric, inputs, DPP edition, model/version, account tier, tools, environment, and time or interaction budget.
2. Create a fresh context for the Control run.
3. Provide the task without DPP and preserve the complete run exactly as returned.
4. Create a second fresh context using the same platform and model.
5. Provide the frozen DPP Operational Edition, then the identical task.
6. Preserve the complete DPP run exactly as returned.
7. Apply the frozen rubric equally to both submissions.
8. Publish the result without repairing either submitted run or changing the rubric afterward.

Randomize run order when practical. Record any retry, interruption, intervention, tool failure, contamination, or deviation.

## Required evidence

A valid result must preserve:

- benchmark identifier and date;
- provider, product, model, and displayed version or build;
- account tier, enabled tools, environment, and budget;
- frozen task, rubric, fixture identifiers, and DPP input;
- complete Control and DPP prompts, transcripts, and outputs;
- tool calls, errors, retries, interruptions, and human intervention;
- start and end commit SHAs when repositories are involved;
- public test output and withheld evaluator output;
- dimension scores with evidence for every deduction;
- critical-failure flags;
- limitations, deviations, and clearly marked redactions.

The evaluator or seeded-defect map must not be shown to either run before submission.

## Integrity rules

- Same task and matched conditions for both runs.
- Fresh context for each condition.
- Control receives no DPP.
- DPP receives the exact frozen Operational Edition before the task.
- First completed submission is the result unless a documented technical failure prevented completion.
- No hidden correction round presented as the original result.
- No weakening tests or changing scoring after seeing outputs.
- No selective publication or removal of unfavorable evidence.
- No generalization beyond the evidence actually produced.

## Benchmark 001 — SafeKeep

The completed paired result and raw outputs are preserved in [`results/benchmark-001/RESULTS.md`](results/benchmark-001/RESULTS.md).

- Control: 35/40
- DPP: 37.5/40
- Difference: +2.5 points
- Relative difference over the Control score: +7.1%

## Benchmark 002 — Production Rescue

The frozen definition is:

- [Task](benchmarks/benchmark-002/TASK.md)
- [Scoring rubric](benchmarks/benchmark-002/SCORING.md)
- [Frozen inputs](benchmarks/benchmark-002/FIXTURE_COMMIT.md)
- [DPP v1.4 Operational Edition](operational/DPP-v1.4-Operational.md)

Benchmark 002 preserves the historical fixture at commit `273946d976c624e4769727d01b719a9f70949b98` and pins the DPP v1.4 Operational Edition by blob and release commit. Its result must be published whether DPP wins, ties, loses, or causes a regression.

## Independent submissions

Independent testers may propose Benchmark 003 or later work using a task-specific rubric established before scoring. The task may remain private when necessary, but both conditions must receive the identical task and the submission must disclose that fact.

Do not reconstruct results from memory, omit embarrassing failures, or convert a case study into a universal claim.
