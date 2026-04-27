# EIP Generated Outputs

Every generated package must be able to produce these output classes.

## 1. C++ Output

Purpose:
- generated `EML` integration code for embedded firmware projects

Minimum expectations:
- model interface/header
- inference or scoring implementation scaffold
- input/output contract mapping
- integration notes for host firmware

## 2. Datasheet-Style Output

Purpose:
- engineering-facing description of the packaged model

Minimum expectations:
- model family
- model category
- input list
- output list
- enabled/disabled wiring state
- target class
- constraints and assumptions

## 3. User-Guide Output

Purpose:
- practical usage guidance for engineers integrating the model package

Minimum expectations:
- setup steps
- configuration summary
- interpretation of outputs
- validation notes
- known assumptions and limits

## Artifact Manifest Rule

All generated outputs must be referenced in the package artifact manifest so the client GUI, code viewer, and future debugger can resolve them consistently.
