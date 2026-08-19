# Benchmark 002 — Production Rescue

## Status

Frozen benchmark definition. Do not change this task, its scoring rubric, the fixture commit, or the DPP input after either run begins.

## Objective

You are inheriting a partially implemented production service. Repair it and deliver a release-ready repository.

You may modify any project file necessary, but you may not weaken, delete, skip, or rewrite tests merely to make them pass.

## Requirements

1. Identify and repair all defects that prevent the service from satisfying its documented contract.
2. Implement all incomplete production functionality. No placeholders, TODO implementations, fake success paths, or hard-coded test answers may remain.
3. Preserve backward compatibility with the documented public API.
4. Reject malformed and unauthorized requests correctly.
5. Prevent duplicate execution when the same valid request is retried.
6. Preserve state correctly across application restart.
7. Prevent concurrent requests from corrupting state or violating invariants.
8. Do not expose secrets or sensitive internal information through responses or logs.
9. Add any tests genuinely necessary to demonstrate the repaired behavior.
10. Produce a concise release report containing:
   - defects discovered;
   - changes made;
   - tests performed and their actual results;
   - remaining limitations or uncertainties;
   - exact commands required to reproduce verification.

## Completion condition

Do not characterize the task as complete unless the repository is actually in a state you would approve for the production release described by its documentation.

If something prevents completion, identify the exact blocker and deliver the strongest verified state achievable without pretending the blocker does not exist.

## Frozen conditions

Both runs use:

- Fixture branch: `benchmark-001-fixture` (historical branch name retained to preserve the immutable fixture).
- Fixture checkout commit: `273946d976c624e4769727d01b719a9f70949b98`.
- Identical model/product/version, account tier, tools, environment, task text, time budget, and interaction budget.
- Fresh context for each run.
- No access to the evaluator or seeded-defect map before submission.

The Control run receives no DPP instructions.

The DPP run receives the complete contents of `operational/DPP-v1.4-Operational.md` before this task:

- Normative file blob SHA: `fafd940cf3952f32bdf89187b36d79afd79cd840`.
- Release commit introducing that file: `7ec35c4a52c343c31b9c94a03487f9296fb61916`.

## Evidence to preserve

- Complete prompts and transcripts.
- Exact DPP input used.
- Start and end commit SHAs.
- Tool calls, errors, retries, interruptions, and human intervention.
- Public test output.
- Withheld evaluator output.
- Release reports.
- Dimension scores, evidence, and deductions.
- Critical-failure flags.

Publish the result whether DPP wins, ties, loses, or causes a regression.
