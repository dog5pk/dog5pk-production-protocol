# Benchmark 002 — Frozen Inputs

- Benchmark: Production Rescue
- Experiment identifier: Benchmark 002
- Historical fixture branch: `benchmark-001-fixture`
- Fixture checkout commit: `273946d976c624e4769727d01b719a9f70949b98`
- Underlying fixture-state commit recorded by the historical fixture: `239fe444315d4cc02abbe168b6379d8496c4e51b`
- Task: `benchmarks/benchmark-002/TASK.md`
- Scoring: `benchmarks/benchmark-002/SCORING.md`
- DPP input: `operational/DPP-v1.4-Operational.md`
- DPP v1.4 blob SHA: `fafd940cf3952f32bdf89187b36d79afd79cd840`
- DPP v1.4 release commit: `7ec35c4a52c343c31b9c94a03487f9296fb61916`

The legacy branch name is retained because rewriting or renaming the original fixture would weaken traceability. Every run must checkout the exact fixture commit, not the moving branch tip.

The benchmark-definition freeze commit is the first repository commit containing this file, `TASK.md`, and `SCORING.md` together. Record that commit SHA in Issue #2 before execution.
