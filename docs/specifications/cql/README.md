# Chart Query Language (CQL)

The **Chart Query Language (CQL)** is the declarative language of the Chartific ecosystem.

CQL provides a human-readable, implementation-independent way to describe the semantic intent of data visualizations. Rather than specifying how a visualization should be rendered, CQL specifies what information should be communicated, allowing the same visualization to be interpreted by any conformant Chartific implementation.

The language is designed to support manual authoring, AI-assisted generation, automated validation, interoperability, and long-term portability.

---

# Purpose

The CQL specification defines the syntax, semantics, and behavior of the Chart Query Language.

It serves as the normative reference for developers implementing:

- CQL parsers
- validators
- formatters
- editors
- language servers
- transpilers
- visualization engines
- Chartific tooling

The specification is implementation independent and does not prescribe rendering technologies or programming languages.

---

# Guiding Principles

CQL is designed according to the following principles:

- Declarative rather than imperative
- Semantic rather than renderer-specific
- Human-readable and AI-friendly
- Deterministic and unambiguous
- Extensible and versionable
- Implementation independent

---

# Specification Structure

The CQL specification is organized into the following parts.

| Part | Description |
|------|-------------|
| Part I | Introduction |
| Part II | Abstract Language Model |
| Part III | Concrete Syntax and Grammar |
| Part IV | Lexical Structure |
| Part V | Semantic Model |
| Part VI | Type System |
| Part VII | Expressions |
| Part VIII | Validation |
| Part IX | Canonical Formatting |
| Part X | Diagnostics |
| Part XI | Conformance |
| Part XII | Extensibility |
| Part XIII | Versioning |
| Appendices | Grammar Reference, Reserved Words, Examples, Change History |

---

# Language Architecture

The CQL specification defines only the language.

Within the Chartific architecture, CQL occupies the authoring layer.

```text
Human / AI Intent
        │
        ▼
Chart Query Language (CQL)
        │
        ▼
Chart Abstraction Model (CAM)
        │
        ▼
Chart Adapter Runtime (CAR)
        │
        ▼
Renderer
```

CQL specifications are transformed into the Chart Abstraction Model (CAM), which serves as the canonical semantic representation consumed by downstream components.

---

# Intended Audience

This specification is intended for:

- language implementers
- parser developers
- compiler and interpreter authors
- IDE and language tooling developers
- visualization platform developers
- AI application developers
- Chartific contributors
- standards authors

---

# Scope

This specification defines:

- the lexical structure of the language;
- the concrete grammar;
- the abstract language model;
- semantic behavior;
- expression evaluation;
- validation rules;
- canonical formatting;
- diagnostics;
- conformance requirements.

This specification does not define:

- rendering algorithms;
- graphics APIs;
- renderer implementations;
- visualization aesthetics;
- application frameworks.

---

# Conformance

An implementation claiming conformance with the Chart Query Language specification shall implement the normative requirements defined within this specification.

Conformance requirements are specified in the **Conformance** section of this specification.

---

# Versioning

The CQL language evolves through versioned specifications.

Each version preserves backward compatibility whenever practical while allowing the language to evolve through well-defined extension mechanisms.

---

# Related Specifications

The Chart Query Language is one component of the Chartific ecosystem.

Related specifications include:

- Chartific Vision
- Chart Abstraction Model (CAM)
- Chart Markup Language (CML)
- Chart Adapter Runtime (CAR)
- Chart Semantic Repository (CSR)
- Chartific Application Server (CAS)
- Chartific Development Kit (CDK)

---

# License

The Chart Query Language specification is published as part of the Chartific Standard.
