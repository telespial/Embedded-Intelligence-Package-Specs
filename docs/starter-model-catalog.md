# EIP Starter Model Catalog

This file defines the first-release starter model set for EmbeddedX.

## Principles

Starter models should:
- work well with structured labels
- fit embedded deployment constraints
- avoid unnecessary complexity
- be easy to explain in the model editor
- map cleanly to generated C++ and runtime artifacts

## Starter Families

### Linear
- `linear`
- `ridge`
- `lasso`
- `logistic`

Use for:
- simple prediction
- classification with low resource cost
- first-pass explainable models

### Tree-Based
- `decision_tree`
- `random_forest`
- `gradient_boosting`

Use for:
- structured multi-signal decision making
- rule-like model behavior
- moderate embedded complexity

### Statistical / Anomaly
- `z_score`
- `ewma`
- `gaussian`
- `isolation_forest`

Use for:
- anomaly scoring
- drift detection
- threshold-aware monitoring

### Naive Bayes
- `naive_bayes`

Use for:
- lightweight probabilistic classification

### Support Vector Machine
- `linear_svm`

Use for:
- lightweight margin-based classification
- embedded-friendly first release scope

### KNN
- `knn`

Use for:
- small datasets
- prototyping
- comparison baselines

### Small Neural Networks
- `small_mlp`

Use for:
- `MPU` / `NPU` targets
- cases where slightly richer learned behavior is needed

## Embedded Constraints

For first release, prefer:
- `0-3` layers
- under `1000` parameters where practical
- explainable outputs and reviewable metadata
