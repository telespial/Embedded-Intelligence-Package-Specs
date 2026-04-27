# EIP Overview

`EIP` defines the deployable package format for EmbeddedX embedded-model workflows.

The package is the shared contract consumed by:
- model selection
- model editing
- package validation
- C++ generation
- datasheet generation
- user-guide generation
- 3D model viewing
- AICS output review
- future debug and deployment flows

## Why This Exists

Without a package contract, each tool invents its own interpretation of:
- model type
- enabled inputs
- enabled outputs
- training metadata
- generated artifacts

`EIP` removes that ambiguity.

## v1 Focus

Version `1` is intentionally narrow:
- up to `16` inputs
- embedded-first model families
- small model bias
- stable repeatable outputs for stable environments
- label-first, train-later workflow

## v1 Consumers

- EmbeddedX Client GUI
- EmbeddedX model editor/generator
- EmbeddedX 3D model viewer
- AICS code/artifact viewer
- future debugger integration
