# Chart Abstraction Model (CAM)

**Status:** Draft (v0.1)

The **Chart Abstraction Model (CAM)** is the canonical semantic model of the Chartific Standard. It defines an implementation-independent representation of visualizations that captures **what** a visualization means rather than **how** it is rendered.

CAM serves as the common semantic language shared by every component of the Chartific ecosystem. It enables applications, AI systems, validation engines, repositories, and visualization platforms to exchange, process, and render visualizations without depending on any specific charting library, framework, or rendering technology.

---

# Overview

Modern visualization libraries require developers to construct charts using renderer-specific configuration models. As a result, equivalent visualizations often need to be recreated for different visualization frameworks, leading to duplicated effort, vendor lock-in, inconsistent behavior, and limited interoperability.

The Chart Abstraction Model addresses this challenge by introducing a universal semantic representation that describes the analytical meaning of a visualization independently of its textual syntax or graphical implementation.

CAM separates **authoring** from **execution**.

Chart Query Language (CQL) provides a human-readable language for authoring visualizations, while CAM provides the canonical semantic representation that can be validated, transformed, serialized, governed, stored, and rendered without reference to the original source language.

Rather than representing graphical primitives such as SVG elements, pixels, drawing commands, or renderer-specific configuration objects, CAM represents visualization semantics, including:

- Data sources
- Measures
- Dimensions
- Time series
- Groupings
- Aggregations
- Transformations
- Analytical intent
- Visual encodings
- Interaction behavior
- Metadata
- Trust information

This semantic representation enables a single visualization definition to be interpreted consistently across multiple rendering technologies through the Chart Adapter Runtime (CAR).

---

# Design Goals

The Chart Abstraction Model is designed to:

- Represent visualization intent independently of rendering technology.
- Provide the canonical semantic representation of Chartific visualizations.
- Serve as a stable intermediate representation between authoring and rendering.
- Enable interoperability across visualization platforms.
- Support AI-native visualization generation, interpretation, and transformation.
- Enable governance, validation, and trust services.
- Preserve visualization semantics throughout the visualization lifecycle.
- Provide a stable foundation for future visualization standards.

---

# Architecture

CAM occupies the semantic layer of the Chartific architecture.

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
Chartific Application Server (CAS)
        │
        ▼
Chart Adapter Runtime (CAR)
        │
        ▼
Visualization Engine
```

A CQL specification is compiled into a CAM object.

The Chartific Application Server (CAS) validates, governs, transforms, and manages the semantic model before delegating rendering to the Chart Adapter Runtime (CAR). The adapter translates the implementation-independent CAM representation into the native configuration required by a supported visualization engine.

---

# Responsibilities

The Chart Abstraction Model is responsible for:

- Representing visualization semantics.
- Defining the canonical visualization object model.
- Providing a stable intermediate representation between authoring and rendering.
- Supporting validation and semantic transformation.
- Enabling serialization and interoperability.
- Preserving visualization meaning throughout its lifecycle.

CAM is **not** responsible for:

- Rendering visualizations.
- Defining authoring syntax.
- Specifying rendering algorithms.
- Managing visualization repositories.
- Implementing visualization libraries.

These responsibilities belong to other components of the Chartific ecosystem.

---

# Core Principles

## Semantic First

Visualizations are represented by their analytical meaning rather than their graphical implementation.

---

## Canonical Representation

Every visualization has a single canonical semantic representation independent of how it was authored or where it is rendered.

---

## Renderer Independence

A CAM object can be rendered by any compatible visualization engine without modification.

---

## AI Native

CAM is designed to be easily generated, interpreted, validated, transformed, and optimized by AI systems.

---

## Extensible

The model supports future visualization types, interaction models, metadata, and domain-specific extensions while maintaining compatibility with existing implementations.

---

## Portable

A CAM object can move between applications, organizations, repositories, and rendering technologies while preserving its semantics.

---

## Deterministic

Equivalent visualizations should produce equivalent semantic models, enabling predictable validation, transformation, and rendering.

---

# Relationship to Other Chartific Components

| Component | Responsibility |
|-----------|----------------|
| **CQL** | Defines visualization intent through a declarative language. |
| **CAM** | Defines the canonical semantic representation of visualizations. |
| **CML** | Serializes CAM for storage and interchange. |
| **CAS** | Processes, validates, governs, and manages CAM objects. |
| **CAR** | Translates CAM into renderer-specific implementations. |
| **CSR** | Stores reusable semantic visualization artifacts. |
| **CGE** | Applies governance, policy, and compliance rules. |
| **CATS** | Verifies visualization authenticity, integrity, and trust. |

---

# Scope

Version **0.1** establishes the core semantic model required to represent visualization intent independently of authoring languages and rendering technologies.

The CAM specification defines:

- The core object model
- Semantic entities
- Object relationships
- Property model
- Expression model
- Validation constraints
- Extension mechanisms
- Normalization rules
- Serialization requirements
- Conformance requirements

The specification intentionally excludes renderer-specific implementation details, rendering algorithms, graphics APIs, and authoring language syntax.

---

# Summary

The Chart Abstraction Model (CAM) is the canonical semantic representation at the core of the Chartific ecosystem.

By separating visualization semantics from authoring languages and rendering technologies, CAM enables interoperable visualization tooling, portable visualization artifacts, AI-native workflows, governance, validation, and consistent semantic interpretation throughout the entire visualization lifecycle.

CAM provides the stable semantic foundation upon which the Chartific ecosystem is built.
