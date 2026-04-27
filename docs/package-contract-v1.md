# EIP Package Contract v1

This document defines the v1 package contract for `Embedded Intelligence Package Specs`.

## 1. Package Identity

Each package must define:
- `packageId`
- `name`
- `version`
- `schemaVersion`
- `createdUtc`

## 2. Model Definition

Each package selects exactly one `modelFamily`.

Allowed starter families:
- `linear`
- `ridge`
- `lasso`
- `logistic`
- `decision_tree`
- `random_forest`
- `gradient_boosting`
- `z_score`
- `ewma`
- `gaussian`
- `isolation_forest`
- `naive_bayes`
- `linear_svm`
- `knn`
- `small_mlp`

Each package must also define:
- `modelCategory`
  - `regression`
  - `anomaly`
  - `adaptive_reasoning`
  - `state_machine`
  - `classification`
  - `future`
- `targetClass`
  - `MCU`
  - `MPU`
  - `NPU`
- `parameterCount`
- `layerCount`

## 3. Inputs

- A package may define up to `16` inputs.
- Every input must declare:
  - `inputId`
  - `name`
  - `enabled`
  - `valueType`
  - `semanticType`
  - `unit`
  - `sourceChannel`
- Inputs can be present but disabled when not wired.

## 4. Outputs

Every output must declare:
- `outputId`
- `name`
- `enabled`
- `valueType`
- `semanticRole`

Outputs must follow the selected model category contract.

### 4.1 Regression outputs
- expected outputs may include:
  - `predicted_value`
  - `confidence_score`
  - `reason_code`

### 4.2 Anomaly outputs
- expected outputs may include:
  - `anomaly_score`
  - `alert_state`
  - `reason_code`

### 4.3 Adaptive reasoning outputs
- expected outputs may include:
  - `recommended_state`
  - `confidence_score`
  - `reason_code`
  - `policy_hint`

### 4.4 State machine outputs
- expected outputs may include:
  - `state_id`
  - `transition_event`
  - `reason_code`

### 4.5 Future families
- future families must still declare explicit output semantics in the package manifest.

## 5. Training Metadata

Each package must define training metadata:
- `trainingMode`
  - `labeled_historical`
  - `on_chip_recorded`
  - `self_learning`
- `labelStrategy`
  - `label_first`
  - `train_first`
- `datasetSummary`
- `notes`

v1 should prioritize `label_first` workflows.

## 6. Artifact Manifest

Each package must include an artifact manifest that can point to:
- generated C++ output
- datasheet-style output
- user-guide output

Each artifact must declare:
- `artifactId`
- `artifactType`
- `path`
- `required`

## 7. Embedded Optimization Intent

v1 packages should reflect:
- small efficient embedded models
- lower training-data needs where possible
- stable repeatable outputs for stable environments
- faster deployment by defining behavior first and training later
