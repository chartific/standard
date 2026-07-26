# Chart Markup Language (CML)

**Status:** Draft (v0.1)

The **Chart Markup Language (CML)** is the canonical serialization format of the Chartific Standard. It provides a portable, structured, and implementation-independent representation of Chart Abstraction Model (CAM) objects for storage, exchange, versioning, validation, and interoperability.

Rather than describing renderer-specific configuration, CML serializes the semantic representation of a visualization, preserving its meaning independently of visualization libraries, rendering technologies, or execution environments.

CML enables semantic visualization artifacts to be exchanged consistently between applications, repositories, services, AI systems, and visualization platforms.

---

# Overview

Modern visualization frameworks define proprietary document formats and configuration schemas for representing charts. Although these formats are effective within their respective ecosystems, they are tightly coupled to specific rendering technologies and cannot be exchanged without translation.

The Chart Markup Language addresses this limitation by defining a standardized serialization format for the Chart Abstraction Model (CAM).

Where CAM defines **what a visualization is**, CML defines **how that semantic model is represented as a portable document**.

This separation allows visualization artifacts to be stored, transmitted, versioned, digitally signed, governed, and reconstructed without losing their semantic meaning.

A CML document may contain:

- Document metadata
- Serialized CAM object model
- Data references
- Visualization metadata
- Interaction definitions
- Annotation metadata
- Governance metadata
- Trust information
- Version information

Because CML represents semantic content rather than renderer-specific configuration, the same document can be interpreted consistently across multiple visualization platforms.

---

# Design Goals

The Chart Markup Language is designed to:

- Provide the canonical serialization format for CAM objects.
- Enable portable exchange of semantic visualization artifacts.
- Preserve visualization semantics during storage and transmission.
- Support interoperability across applications and platforms.
- Enable governance, validation, and trust services.
- Support versioning and collaborative workflows.
- Remain independent of rendering technologies and programming languages.

---

# Architecture

CML occupies the serialization layer of the Chartific architecture.

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
Chart Markup Language (CML)
        │
        ▼
Chartific Application Server (CAS)
        │
        ▼
Chart Adapter Runtime (CAR)
        │
        ▼
Visualization Engine
```

A CQL specification is compiled into a CAM object.

The CAM object may be serialized as a CML document for storage, interchange, governance, or versioning. When required, the document is deserialized to reconstruct the original semantic model before validation, transformation, or rendering.

---

# Responsibilities

The Chart Markup Language is responsible for:

- Serializing CAM objects.
- Defining a portable document structure.
- Supporting long-term storage and interchange.
- Preserving semantic integrity during serialization.
- Enabling metadata, governance, and trust information.
- Supporting versioning and interoperability.

CML is **not** responsible for:

- Defining visualization semantics.
- Rendering visualizations.
- Executing visualization logic.
- Defining visualization authoring syntax.
- Implementing visualization libraries.

These responsibilities belong to other Chartific components.

---

# Core Principles

## Semantic Preservation

CML preserves the semantics defined by the Chart Abstraction Model without introducing renderer-specific information.

---

## Canonical Serialization

Equivalent CAM objects should produce equivalent serialized representations, enabling deterministic storage, comparison, and interchange.

---

## Portable

A CML document can move between applications, repositories, organizations, and visualization platforms without modification.

---

## Renderer Independent

CML never depends on renderer-specific APIs, configuration formats, or visualization libraries.

---

## Human and Machine Readable

CML is designed to be understandable by developers while remaining efficient for software systems and AI applications.

---

## Extensible

The document model supports future metadata, extensions, and domain-specific capabilities while preserving compatibility with existing documents.

---

## Versioned

Every CML document explicitly identifies the Chartific specification version to which it conforms.

---

# Relationship to Other Chartific Components

| Component | Responsibility |
|-----------|----------------|
| **CQL** | Defines visualization intent through a declarative language. |
| **CAM** | Defines the canonical semantic representation of visualizations. |
| **CML** | Serializes CAM into a portable document format. |
| **CAS** | Processes, validates, governs, and manages CML documents. |
| **CAR** | Translates CAM into renderer-specific implementations. |
| **CSR** | Stores, indexes, and versions serialized visualization artifacts. |
| **CGE** | Applies governance and policy rules to CML documents. |
| **CATS** | Verifies document authenticity, integrity, and trust. |

---

# Typical Lifecycle

A CML document typically progresses through the following lifecycle.

```text
Human / AI Intent
        │
        ▼
Author Visualization (CQL)
        │
        ▼
Compile to CAM
        │
        ▼
Serialize as CML
        │
        ▼
Store in CSR
        │
        ▼
Validate & Govern
        │
        ▼
Apply Trust Services
        │
        ▼
Deserialize to CAM
        │
        ▼
Render via CAR
```

Throughout this lifecycle, the document remains a portable serialization of the underlying semantic model.

---

# Scope

Version **0.1** establishes the standardized serialization format for Chart Abstraction Model (CAM) objects.

The CML specification defines:

- Document structure
- Serialization rules
- Required metadata
- Document identifiers
- Version information
- Extension mechanisms
- Governance metadata
- Trust metadata
- Conformance requirements

The specification intentionally excludes visualization semantics, rendering algorithms, authoring language syntax, and renderer-specific implementation details.

---

# Summary

The Chart Markup Language (CML) is the canonical serialization format of the Chartific Standard.

By providing a portable, implementation-independent representation of Chart Abstraction Model (CAM) objects, CML enables visualization artifacts to be stored, exchanged, versioned, governed, validated, and trusted without dependence on any specific visualization technology.

Together with CQL and CAM, CML forms one of the core architectural layers of the Chartific ecosystem, enabling semantic visualizations to become portable, interoperable, and durable digital assets.
