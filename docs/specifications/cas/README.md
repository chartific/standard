# Chartific Application Server (CAS)

**Status:** Draft (v0.1)

The **Chartific Application Server (CAS)** is the execution engine of the Chartific Standard. It provides a unified runtime environment responsible for processing chart requests, executing CQL, managing semantic chart lifecycles, enforcing governance policies, validating trust, and orchestrating renderer-independent visualization through the Chart Adapter Runtime (CAR).

CAS serves as the operational heart of the Chartific ecosystem. It transforms semantic chart definitions into managed, secure, and portable visualization services that can be consumed by applications, AI agents, APIs, and enterprise platforms.

---

# Overview

Modern visualization platforms tightly couple data access, business logic, rendering, governance, and application integration into a single charting library. This approach makes visualizations difficult to reuse, govern, audit, or migrate across technologies.

The Chartific Application Server addresses these challenges by introducing a centralized execution environment dedicated to semantic visualization.

Instead of embedding chart generation logic directly within applications, CAS provides a standardized server responsible for:

- Executing Chart Query Language (CQL)
- Managing semantic chart definitions
- Coordinating rendering
- Applying governance policies
- Verifying trust and authenticity
- Serving charts through standardized APIs and MCP

Applications no longer communicate directly with visualization libraries. Instead, they interact with CAS, which becomes the authoritative execution environment for all Chartific operations.

---

# Design Goals

The Chartific Application Server is designed to:

- Execute CQL requests consistently.
- Build and manage Chart Abstraction Models (CAM).
- Coordinate renderer-independent visualization.
- Provide centralized governance and policy enforcement.
- Support AI-native visualization workflows.
- Expose visualization services through APIs and MCP.
- Serve as the operational runtime for the entire Chartific platform.

---

# Position Within the Chartific Architecture

CAS is the central orchestration layer of the Chartific platform.

```text
               Human / AI
                    │
                    ▼
                 Generate CQL
                    │
                    ▼
          Chartific Application Server
                   (CAS)
        ┌───────────┼────────────┐
        │           │            │
        ▼           ▼            ▼
      Compile     Validate    Govern
      to CAM        CATS        CGE
        │
        ▼
     Serialize
      to CML
        │
        ▼
        CSR
        │
        ▼
        CAR
        │
        ▼
 Any Visualization Engine
```

CAS orchestrates every major component of the Chartific ecosystem. It receives visualization requests, manages semantic processing, applies governance and trust validation, retrieves semantic assets from CSR, and delegates rendering through CAR.

---

# Core Principles

## Semantic Execution

CAS executes semantic chart definitions rather than renderer-specific configuration objects.

## Centralized Orchestration

All visualization operations are coordinated through a single execution environment.

## AI Native

CAS is designed to operate seamlessly with AI agents, enabling automated chart generation, validation, transformation, and explanation.

## Renderer Independence

Applications interact only with CAS. Renderer selection is delegated to CAR.

## Stateless by Default

CAS should remain stateless whenever possible, relying on CSR for persistent storage and enabling horizontal scalability.

## Enterprise Ready

CAS is designed to support governance, auditing, authentication, authorization, and organizational policies required in enterprise environments.

---

# Responsibilities

CAS is responsible for:

- Parsing and executing CQL
- Building CAM objects
- Managing CML serialization
- Retrieving and storing charts in CSR
- Invoking CAR for rendering
- Applying governance rules through CGE
- Validating trust signatures through CATS
- Exposing REST, gRPC, CLI, SDK, and MCP interfaces
- Managing chart lifecycle operations
- Returning rendered visualization results

CAS acts as the control plane for the Chartific ecosystem.

---

# Supported Interfaces

CAS provides multiple interfaces to accommodate different consumers.

These include:

- REST APIs
- gRPC APIs
- Native SDKs
- Command Line Interface (CLI)
- MCP Server
- WebSocket streaming
- Background workers
- Scheduled execution

Each interface interacts with the same semantic execution engine, ensuring consistent behavior across environments.

---

# MCP Integration

One of the defining capabilities of CAS is its native support for the **Model Context Protocol (MCP)**.

CAS exposes semantic visualization capabilities as MCP tools, allowing AI assistants and autonomous agents to interact with Chartific using standardized protocols.

Typical MCP operations may include:

- Execute CQL
- Retrieve charts
- Render charts
- Search semantic repositories
- Validate authenticity
- Explain chart semantics
- Compare chart versions
- Publish certified charts

This enables AI systems to create, modify, discover, and validate charts without requiring knowledge of renderer-specific APIs.

---

# Relationship to Other Chartific Components

| Component | Purpose |
|-----------|---------|
| **CQL** | Defines chart intent through declarative queries. |
| **CAM** | Represents semantic chart definitions. |
| **CML** | Serializes semantic charts into portable documents. |
| **CSR** | Stores semantic chart artifacts. |
| **CAR** | Renders semantic charts using supported visualization frameworks. |
| **CGE** | Applies governance, compliance, and policy validation. |
| **CATS** | Verifies authenticity, integrity, and trust. |
| **CAS** | Orchestrates the execution of all Chartific components. |

---

# Execution Lifecycle

A typical visualization request follows this lifecycle:

```text
Receive Request
        │
        ▼
Authenticate
        │
        ▼
Parse CQL
        │
        ▼
Build CAM
        │
        ▼
Validate
        │
        ▼
Apply Governance
        │
        ▼
Retrieve / Store in CSR
        │
        ▼
Verify Trust
        │
        ▼
Invoke CAR
        │
        ▼
Generate Renderer Output
        │
        ▼
Return Result
```

This lifecycle provides a consistent execution model regardless of the underlying visualization technology.

---

# Monolithic Binary Architecture

The reference implementation of CAS is designed as a **single self-contained executable**.

Inspired by infrastructure platforms such as Prometheus, CAS bundles all core functionality into one deployable binary, including:

- CQL execution
- Semantic processing
- Repository integration
- Governance
- Trust validation
- Adapter management
- API server
- MCP server
- Administration interface

This architecture simplifies deployment, minimizes operational complexity, and enables organizations to adopt Chartific without assembling multiple services.

Additional capabilities may be enabled through configuration rather than requiring separate deployments.

---

# Scope

Version **0.1** of CAS focuses on defining the standardized execution environment for semantic visualization.

The initial specification establishes:

- Runtime architecture
- Execution lifecycle
- Service interfaces
- Component orchestration
- Adapter integration
- Repository integration
- Governance workflow
- Trust workflow
- MCP integration

Future versions may introduce:

- Distributed execution
- High-availability clustering
- Multi-tenant deployments
- Cloud-native orchestration
- Plugin ecosystems
- Workflow automation
- Event-driven execution
- Serverless deployments

while maintaining backward compatibility.

---

# Future Specification

This document serves as an introduction to the Chartific Application Server.

The complete CAS specification will define:

- Server architecture
- Runtime model
- Service interfaces
- API specifications
- MCP implementation
- Configuration model
- Deployment architecture
- Security model
- Authentication and authorization
- Extension framework
- Operational guidelines
- Compatibility requirements

---

# Summary

The Chartific Application Server (CAS) is the operational core of the Chartific Standard. It provides a unified execution environment that transforms semantic chart definitions into secure, governed, trustworthy, and renderer-independent visualization services.

By centralizing execution, integrating AI through MCP, orchestrating semantic processing, and adopting a monolithic binary architecture, CAS establishes the runtime foundation upon which the entire Chartific ecosystem is built.
