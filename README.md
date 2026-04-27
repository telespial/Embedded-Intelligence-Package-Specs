# Embedded Intelligence Package (EIP)

Embedded Intelligence Package (`EIP`) defines the deployable package contract for EmbeddedX model systems.

It standardizes how an embedded model package describes:
- model family
- enabled inputs
- enabled outputs
- training metadata
- generated artifacts
- compatibility and runtime assumptions

`EIP` is the package layer that sits between model definition and client-side generation/view/debug workflows.

## v1 Goals

Version `1` of the package contract is optimized for the first EmbeddedX client workflow:
- up to `16` inputs
- input and output wiring can be enabled or disabled explicitly
- model-family-specific output contracts
- generated artifact manifest for:
  - C++ output
  - datasheet-style output
  - user-guide output
- small embedded-focused model families
- label-first, train-later workflow support

## Relationship To Other Specifications

- `EmbeddedX-Specs` — umbrella index
- `MRD` — machine-readable hardware structure
- `MRC` — connectivity structure
- `MDP` — model definition contract
- `EIL` / `EML` runtime concepts
- `AICS` — code and workflow orchestration surface

Use `embedded-intelligence-layer` as the reference for editor/build/export UX.
Use `codemaster` as the reference for schema discipline, manifest layout, and validation structure.

## Repository Layout

- `docs/overview.md` — scope and system role
- `docs/package-contract-v1.md` — normative v1 package contract
- `docs/starter-model-catalog.md` — first-release model families
- `docs/generated-outputs.md` — required generated artifacts
- `docs/manifest.md` — manifest rules
- `docs/compatibility.md` — compatibility rules
- `schemas/eip.package.schema.json` — v1 package schema
- `examples/example.eip.json` — example package

## v1 Core Rules

An `EIP` package must:
- declare a single selected model family
- support up to `16` inputs
- declare enable/disable wiring state for each input and output
- describe generated outputs through an artifact manifest
- carry enough metadata for the client GUI, generator, viewer, and debugger to consume the same package consistently

## First-Release Starter Model Families

- Linear:
  - linear
  - ridge
  - lasso
  - logistic
- Tree-based:
  - decision_tree
  - random_forest
  - gradient_boosting
- Statistical / anomaly:
  - z_score
  - ewma
  - gaussian
  - isolation_forest
- `naive_bayes`
- `linear_svm`
- `knn`
- `small_mlp` for `MPU` / `NPU` targets

## License

See `LICENSE.md`.
