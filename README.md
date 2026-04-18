# Embedded Intelligence Package (EIP)

[← Back to EmbeddedX-Specs (canonical index)](https://github.com/telespial/EmbeddedX-Specs)

## Packaging for Deployable Embedded AI Artifacts

Proposed by: Richard Haberkern  
Contact: rmhaberkern@gmail.com

Free for evaluation. Commercial use requires permission. See [LICENSE.md](./LICENSE.md) for more information.

Part of the **EmbeddedX specification family**.

**Canonical index:** start at `EmbeddedX-Specs`:
https://github.com/telespial/EmbeddedX-Specs

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

## 3. Relationship to Other Specifications

* **EmbeddedX (umbrella):** https://github.com/telespial/EmbeddedX-Specs
* **MRD:** https://github.com/telespial/Machine-Readable-Datasheets-Specs
* **MRC:** https://github.com/telespial/Machine-Readable-Connectivity-Specs
* **MDP:** https://github.com/telespial/Model-Definition-Package-Specs
* **EIL:** https://github.com/telespial/Embedded-Intelligence-Layer-Specs
* **AICS:** https://github.com/telespial/AI-Coding-System-Specs

* * *

## 4. Core Principle

A deployable package should be structured, inspectable, and explicit about what it contains.

* * *

## License

See [LICENSE.md](./LICENSE.md).
