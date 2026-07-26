# Contributing to Chartific

**Status:** Draft

Thank you for your interest in contributing to **Chartific**.

Chartific is an open standard initiative focused on creating a universal semantic visualization ecosystem where charts become portable, interoperable, governed, and trustworthy digital assets.

The goal of Chartific is not simply to create another charting library. Instead, Chartific aims to establish a complete visualization standard built around:

- **CQL** — Chart Query Language
- **CAM** — Chart Abstraction Model
- **CML** — Chart Markup Language
- **CSR** — Chart Semantic Repository
- **CAR** — Chart Adapter Runtime
- **CAS** — Chartific Application Server
- **CGE** — Chart Governance Engine
- **CATS** — Chart Authenticity and Trust Signature
- **CDK** — Chartific Development Kit
- **Chartific MCP Profile** — AI agent integration layer

Contributions are welcome from developers, architects, researchers, data professionals, AI practitioners, visualization experts, and organizations interested in building the future of semantic visualization.

---

# Ways to Contribute

Chartific is a multi-disciplinary standard. Contributions are not limited to software development.

The project welcomes contributions in the following areas:

## Specification Contributions

The Chartific specifications define the foundation of the standard.

Examples:

- Improving CQL grammar.
- Extending CAM semantic models.
- Defining CML schemas.
- Improving CAR adapter specifications.
- Defining CAS architecture.
- Enhancing governance models.
- Improving trust and certification mechanisms.

Specification contributions should focus on:

- Clarity
- Interoperability
- Long-term stability
- Backward compatibility
- Industry applicability

---

## Software Contributions

Software contributions may include:

- Reference implementations.
- SDK development.
- Runtime components.
- Adapter implementations.
- Developer tooling.
- Testing frameworks.
- Documentation tooling.

Examples:

- Implementing a CQL parser.
- Building a CAM validation engine.
- Creating a Chart.js adapter.
- Developing language SDKs.
- Improving CAS performance.

---

## Documentation Contributions

Documentation is a critical part of establishing an open standard.

Contributions may include:

- Improving technical documentation.
- Writing tutorials.
- Creating examples.
- Clarifying specifications.
- Improving developer onboarding.

---

## Research Contributions

Chartific welcomes research contributions related to:

- Semantic visualization.
- AI-generated visualization.
- Visualization standards.
- Human-computer interaction.
- Data governance.
- Trust frameworks.
- Visualization interoperability.

---

# Contribution Philosophy

Chartific follows these principles:

## Standards Before Implementations

The project prioritizes defining stable, interoperable standards before creating implementations.

A good standard should allow multiple implementations to coexist.

---

## Open Collaboration

Chartific aims to encourage participation from individuals and organizations.

Ideas should be evaluated based on:

- Technical merit.
- Interoperability.
- Long-term value.
- Community benefit.

---

## Simplicity Over Complexity

Contributions should avoid unnecessary complexity.

A successful standard should be:

- Easy to understand.
- Easy to implement.
- Easy to adopt.

---

## Backward Compatibility

Changes to existing specifications should carefully consider existing implementations.

Breaking changes should require strong justification.

---

# Repository Structure

The Chartific repository is organized into several areas:

```text
chartific/
│
├── docs/
│   └── specifications/
│       ├── cql/
│       ├── cam/
│       ├── cml/
│       ├── csr/
│       ├── car/
│       ├── cas/
│       ├── cge/
│       ├── cats/
│       ├── cdk/
│       └── mcp-profile/
│
├── examples/
│
├── reference/
│
├── sdk/
│
└── tests/
```

Each area has a specific purpose:

| Directory | Purpose |
|---|---|
| `docs/specifications` | Formal Chartific specifications |
| `examples` | Usage examples and demonstrations |
| `reference` | Reference implementations |
| `sdk` | Language-specific development kits |
| `tests` | Validation and compatibility testing |

---

# Before Contributing

Before starting a contribution:

1. Review the existing documentation.
2. Understand the relevant Chartific component.
3. Search existing issues and discussions.
4. Determine whether the change affects specifications, implementations, or documentation.
5. Create a proposal for significant architectural changes.

---

# Contribution Workflow

The general workflow is:

```text
Idea
 │
 ▼
Discussion
 │
 ▼
Proposal
 │
 ▼
Implementation
 │
 ▼
Review
 │
 ▼
Merge
 │
 ▼
Release
```

---

# Issues

GitHub Issues should be used for:

- Bug reports.
- Feature requests.
- Specification improvements.
- Documentation improvements.
- Implementation discussions.

A good issue should include:

- Clear description.
- Problem being solved.
- Expected behavior.
- Relevant examples.
- Possible implementation approach.

---

# Pull Requests

All changes should be submitted through pull requests.

A pull request should include:

- Clear title.
- Description of the change.
- Reason for the change.
- Related issue references.
- Testing information where applicable.

---

# Pull Request Guidelines

Good pull requests should:

- Solve one focused problem.
- Include appropriate documentation.
- Include tests where applicable.
- Avoid unrelated changes.
- Maintain existing style conventions.

Large architectural changes should be discussed before implementation.

---

# Specification Change Process

Changes to Chartific specifications follow a more structured process.

A specification change should include:

## Problem Statement

Explain:

- What problem exists?
- Why is change required?

---

## Proposed Solution

Explain:

- New behavior.
- Technical approach.
- Compatibility considerations.

---

## Alternatives Considered

Document:

- Other approaches.
- Advantages.
- Disadvantages.

---

## Impact Analysis

Describe impact on:

- Existing implementations.
- Developers.
- Organizations.
- Future compatibility.

---

# RFC Process

Significant changes should follow a Request for Comments (RFC) process.

Example:

```text
RFC-0001: Initial CQL Grammar
RFC-0002: CAM Object Model Extensions
RFC-0003: CML Serialization Format
RFC-0004: Chartific MCP Profile
```

An RFC should provide enough information for the community to evaluate the proposal.

---

# Code Standards

Software contributions should prioritize:

- Readability.
- Maintainability.
- Security.
- Performance.
- Testability.

Code should include:

- Documentation.
- Tests.
- Examples where appropriate.

---

# Testing Requirements

Contributors should validate changes before submission.

Testing may include:

- Unit tests.
- Integration tests.
- Specification validation.
- Compatibility testing.
- Example execution.

A contribution should not introduce regressions into existing functionality.

---

# Documentation Standards

Documentation should be:

- Clear.
- Precise.
- Technical.
- Accessible.

Avoid:

- Vendor-specific assumptions.
- Unnecessary complexity.
- Ambiguous terminology.

When introducing new concepts:

- Define the term.
- Explain the purpose.
- Provide examples.

---

# Community Conduct

Chartific contributors are expected to maintain a professional and respectful environment.

Contributors should:

- Respect different technical opinions.
- Focus discussions on ideas rather than individuals.
- Provide constructive feedback.
- Encourage collaboration.

Disagreements should be resolved through technical discussion and evidence.

---

# Maintainers

Maintainers are responsible for:

- Reviewing contributions.
- Maintaining project quality.
- Managing releases.
- Protecting specification integrity.
- Supporting contributors.

Maintainers should prioritize:

- Openness.
- Transparency.
- Technical excellence.
- Long-term sustainability.

---

# Becoming a Maintainer

Regular contributors may become maintainers based on:

- Quality of contributions.
- Technical expertise.
- Community involvement.
- Understanding of Chartific principles.

Maintainer responsibilities include:

- Reviewing changes.
- Supporting contributors.
- Maintaining project standards.

---

# Recognition

Chartific values all contributions.

Contributors may be recognized through:

- Contributor listings.
- Release notes.
- Project acknowledgements.
- Specification credits.

---

# Long-Term Vision

Chartific aims to become an open standard for semantic visualization.

Achieving this requires collaboration across:

- Developers.
- AI researchers.
- Visualization experts.
- Enterprise organizations.
- Open-source communities.

Every contribution helps move visualization from isolated charts toward a universal, portable, trusted semantic ecosystem.

---

# Summary

Contributing to Chartific means participating in the creation of an open visualization standard.

Whether contributing specifications, software, documentation, research, or ideas, every contribution helps establish a future where charts are:

- Portable.
- Interoperable.
- Governed.
- Authentic.
- AI-native.
- Trusted.

Together, the Chartific community can build the foundation for the next generation of visualization technology.
