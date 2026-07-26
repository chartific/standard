# Chartific Development Kit (CDK)

**Status:** Draft (v0.1)

The **Chartific Development Kit (CDK)** is the official software development toolkit of the Chartific Standard. It provides language-native APIs, libraries, and tooling that enable developers to build applications on top of the Chartific ecosystem without interacting directly with renderer-specific charting libraries.

The CDK abstracts the complexity of semantic visualization by exposing a consistent developer experience across programming languages, frameworks, and platforms. Developers express chart intent using Chart Query Language (CQL) or the Chartific APIs, while the CDK communicates with the Chartific Application Server (CAS) to manage the complete visualization lifecycle.

---

# Overview

Modern applications often require direct integration with multiple charting libraries, each providing its own programming model, configuration syntax, lifecycle, and rendering APIs. Supporting multiple visualization frameworks typically results in duplicated logic, increased maintenance, and vendor lock-in.

The Chartific Development Kit addresses this challenge by providing a standardized programming interface that abstracts the underlying Chartific platform.

Instead of writing renderer-specific code, developers use a language-native SDK that communicates with CAS, executes CQL, retrieves semantic chart definitions, manages chart lifecycle operations, and renders charts through the Chart Adapter Runtime (CAR).

This enables developers to focus on business logic rather than visualization infrastructure.

---

# Design Goals

The Chartific Development Kit is designed to:

- Provide a consistent developer experience across programming languages.
- Abstract communication with the Chartific Application Server.
- Simplify execution of CQL.
- Support AI-native application development.
- Eliminate direct dependencies on visualization frameworks.
- Provide strongly typed APIs where supported.
- Enable rapid application development.

---

# Position Within the Chartific Architecture

CDK is the application integration layer of the Chartific platform.

```text
Application
      │
      ▼
     CDK
      │
      ▼
     CAS
      │
      ▼
     CAM
      │
      ▼
     CAR
      │
      ▼
Any Visualization Engine
```

Applications interact exclusively with the CDK. The CDK communicates with CAS, which performs semantic processing, governance, trust validation, repository access, and rendering orchestration.

This architecture keeps applications independent of visualization technologies while ensuring consistent behavior across platforms.

---

# Core Principles

## Language Native

Every CDK implementation should feel natural within its target programming language, following established language conventions, idioms, and best practices.

## Consistent API

Although each language has its own style, all official CDKs should expose a consistent conceptual programming model.

## Renderer Independent

Applications built with the CDK should never depend directly on renderer-specific APIs or configuration objects.

## AI Ready

The CDK should enable seamless integration with AI agents capable of generating, modifying, validating, and explaining semantic visualizations.

## Minimal Surface Area

The CDK should expose high-level semantic operations rather than low-level rendering details, keeping the developer experience simple and expressive.

---

# Responsibilities

The CDK is responsible for:

- Connecting to CAS.
- Executing CQL.
- Managing authentication.
- Uploading and retrieving CML documents.
- Searching semantic repositories.
- Managing chart lifecycle operations.
- Rendering charts through CAS.
- Invoking MCP operations where supported.
- Handling errors and compatibility information.
- Providing language-native abstractions.

The CDK intentionally avoids implementing visualization logic locally. Rendering responsibilities remain within the Chartific platform.

---

# Supported Programming Languages

The Chartific Standard aims to provide official CDKs for major programming ecosystems.

Initial target languages include:

- TypeScript / JavaScript
- Python
- Java
- C#
- Go
- Rust
- Kotlin
- Swift
- PHP
- Dart

Additional community-maintained implementations may extend support to other languages while conforming to the CDK specification.

---

# Relationship to Other Chartific Components

| Component | Purpose |
|-----------|---------|
| **CQL** | Defines chart intent through declarative queries. |
| **CAM** | Represents semantic chart definitions. |
| **CML** | Provides the portable document format for semantic charts. |
| **CSR** | Stores semantic chart artifacts. |
| **CAR** | Renders semantic charts using supported visualization frameworks. |
| **CAS** | Executes semantic visualization workflows. |
| **CDK** | Provides language-native APIs for interacting with the Chartific platform. |
| **CGE** | Applies governance and organizational policies. |
| **CATS** | Verifies chart authenticity and trust. |

---

# Developer Workflow

A typical application workflow follows these steps:

```text
Application
      │
      ▼
Initialize CDK
      │
      ▼
Authenticate
      │
      ▼
Execute CQL
      │
      ▼
Receive Chart
      │
      ▼
Render
      │
      ▼
Interact
```

The application never interacts directly with Chart.js, D3, Syncfusion, or any other visualization framework.

---

# SDK Architecture

Every official CDK should provide a common architecture consisting of:

- Client initialization
- Authentication
- CQL execution
- Chart management
- Repository operations
- Rendering requests
- Search APIs
- Governance APIs
- Trust verification
- MCP client integration
- Error handling
- Configuration management

While implementation details may vary between programming languages, the conceptual model should remain consistent.

---

# MCP Integration

The CDK provides first-class support for the **Model Context Protocol (MCP)**.

Applications and AI agents can invoke Chartific capabilities using standardized MCP interfaces without requiring knowledge of REST endpoints or renderer-specific APIs.

Example capabilities include:

- Execute semantic chart queries.
- Retrieve charts from CSR.
- Validate authenticity.
- Explain chart semantics.
- Search visualization assets.
- Compare chart versions.
- Publish certified charts.
- Discover available renderers.

By integrating MCP directly into the CDK, Chartific enables AI-native software development where intelligent agents can participate as first-class consumers of the visualization platform.

---

# Scope

Version **0.1** of the CDK focuses on defining a unified programming model for interacting with the Chartific ecosystem.

The initial specification establishes:

- Client architecture
- Authentication model
- Programming conventions
- CQL execution
- Repository operations
- Rendering requests
- Error handling
- Configuration model
- MCP integration

Future versions may introduce:

- Offline execution
- Local development mode
- Streaming visualizations
- Reactive APIs
- Code generation
- Framework-specific integrations
- IDE tooling
- AI-assisted development features

while maintaining backward compatibility.

---

# Future Specification

This document serves as an introduction to the Chartific Development Kit.

The complete CDK specification will define:

- Programming model
- Client lifecycle
- Language compatibility
- API conventions
- Authentication
- Error model
- Configuration
- MCP integration
- Version compatibility
- Extension mechanisms
- Packaging guidelines

---

# Summary

The Chartific Development Kit (CDK) is the official developer interface to the Chartific ecosystem. It enables applications to create, discover, manage, and render semantic visualizations using consistent language-native APIs while remaining completely independent of renderer-specific charting libraries.

Together with CAS, CQL, CAM, and the rest of the Chartific Standard, the CDK establishes a unified programming model for building AI-native, portable, governed, and trustworthy visualization applications across every major programming language.
