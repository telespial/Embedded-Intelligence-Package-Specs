# EIP Compatibility

Compatibility must be explicit.

A package must declare:
- schema version
- supported runtime class
- supported target class:
  - `MCU`
  - `MPU`
  - `NPU`
- model-family constraints
- generated artifact set
- optional dependency assumptions

## v1 Embedded Constraints

First-release packages should prioritize:
- `0-3` layers where applicable
- under `1000` parameters where practical
- deterministic or reviewable output semantics
- embedded deployment rather than generic cloud AI assumptions

## Validation Expectation

Compatibility validation should fail when:
- input count exceeds `16`
- output contract does not match model family
- required generated artifacts are missing
- target class is incompatible with the selected model family
