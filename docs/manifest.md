# EIP Manifest

Each package must define a manifest with the following minimum sections:

- `package`
  - package name
  - package version
  - schema version
  - package id
- `model`
  - selected model family
  - model type
  - target class
  - layer/parameter metadata
- `inputs`
  - up to `16` input definitions
  - enabled/disabled wiring state
  - type, unit, and semantic role
- `outputs`
  - enabled/disabled output definitions
  - output contract by model type
- `training`
  - training mode
  - label-first metadata
  - dataset source summary
- `artifacts`
  - generated C++ output
  - datasheet-style output
  - user-guide output
- `compatibility`
  - runtime assumptions
  - target profile
  - package dependencies

The manifest is the single source of truth for package inspection and downstream generation.
