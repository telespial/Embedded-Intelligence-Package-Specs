# Embedded Intelligence Package (EIP)

## Packaging for Deployable Embedded AI Artifacts

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See license.md for more information.

Part of the [EmbeddedX platform](https://github.com/telespial/EmbeddedX-Specs).

* * *

## Abstract

Embedded Intelligence Package (EIP) defines how to package deployable embedded AI artifacts, including model metadata, runtime assets, and integration guidance. It is meant to cover the files an engineer actually needs to move from a model definition to something usable in a project.

EIP sits closer to deployment than the pure contract repositories and makes that role explicit.

* * *

## 1. Scope

EIP may package:

* model artifacts
* MDP-linked metadata
* EIL-linked runtime integration assets
* documentation for integration
* deployment notes
* validation summaries
* package manifests
* version and compatibility notes

* * *

## 2. Why EIP Matters

Specifications alone are not enough when engineers need a deployable, inspectable bundle. EIP establishes a consistent packaging layer so deployable intelligence does not become an ad hoc folder of half-documented files.

* * *

## 3. Relationship to Other Repositories

* [EmbeddedX-Specs](https://github.com/telespial/EmbeddedX-Specs) establishes the umbrella platform
* [Machine-Readable-Datasheets-Specs](https://github.com/telespial/Machine-Readable-Datasheets-Specs) may shape hardware-facing deployment assumptions
* [Machine-Readable-Connectivity-Specs](https://github.com/telespial/Machine-Readable-Connectivity-Specs) may contribute MRC-linked deployment metadata, compatibility notes, and board-specific integration documentation
* [Model-Definition-Package-Specs](https://github.com/telespial/Model-Definition-Package-Specs) establishes model contract content that may be packaged
* [Embedded-Intelligence-Layer-Specs](https://github.com/telespial/Embedded-Intelligence-Layer-Specs) establishes runtime integration expectations that may be packaged
* [AI-Integrated-Coding-System-Spec](https://github.com/telespial/AI-Integrated-Coding-System-Spec) may generate artifacts that end up in an EIP

* * *

## 4. Core Principle

A deployable package should be structured, inspectable, and explicit about what it contains.

* * *

## License

See `license.md`.
