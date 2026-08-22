# Architecture

## Conceptual model

```text
Feature
  └─ Pattern
      └─ Standard
          └─ Template
              └─ Variant / project-specific extension
```

The model is intentionally conceptual. A real feature may have multiple Patterns, a Pattern may be governed by multiple Standards, and a Template may implement multiple Standards. The repository should avoid forcing a false one-to-one relationship when the domain requires composition.

## Definitions

### Feature
A user/business-facing capability, such as Authentication, File Upload, Search, or Notification.

### Pattern
A recognized way of solving a Feature, such as Email + Password, OAuth, or Passkey authentication.

### Standard
The reusable rules and quality constraints that define the expected behavior, security, contracts, validation, testing, and non-functional requirements for a Pattern or cross-cutting concern.

### Template
A reusable implementation artifact for a concrete technology stack. A Template must identify the Standard(s) it implements and its supported stack/version assumptions.

### Variant
A controlled deviation or extension needed for a specific requirement. Variants should be generalized and promoted when evidence shows they represent a reusable pattern.

## Layers

### Catalog layer
`catalog/` answers: **What capabilities and patterns exist?**

### Standard layer
`standards/` answers: **What must be true?**

### Pattern layer
`patterns/` answers: **Which recognized solution are we selecting?**

### Template layer
`templates/` answers: **How is the selected solution implemented in this technology?**

### Variant layer
`variants/` answers: **How do we safely handle requirements outside the common path?**

### Schema layer
`schemas/` answers: **How can humans and machines represent and validate these definitions?**

## Technology boundary

A technology-neutral requirement belongs in the conceptual layers. Framework-specific code, configuration, dependency versions, and integration details belong in Templates or clearly technology-scoped Patterns.

## AI selection target

The eventual AI workflow should transform a natural-language requirement into a structured selection:

```text
Requirement
  ↓
Feature identification
  ↓
Pattern selection
  ↓
Standard/constraint selection
  ↓
Template selection
  ↓
Variant detection
  ↓
Implementation plan
```

The AI should not invent a new pattern when an existing Standard/Pattern satisfies the requirement. If no suitable pattern exists, the AI should identify the gap and propose a new Variant/Pattern through the repository workflow.

## Evolution model

```text
Standard
   ↓
Real use
   ↓
Gap / exception
   ↓
Variant
   ↓
Repeated use + generalization
   ↓
Pattern / Standard promotion
```

This prevents both uncontrolled duplication and premature over-standardization.
