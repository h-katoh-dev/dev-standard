# dev-standard

Reusable development standards, patterns, and implementation templates for application and web development.

## Vision

Reduce repeated development effort by turning recurring engineering decisions into reusable, testable, machine-readable standards that can eventually be selected and assembled through AI dialogue.

## Model

`Feature → Pattern → Standard → Template → Variant`

The repository is designed to evolve from a human-maintained standard library into an AI-accessible development foundation.

## Mandatory rules

This is a **public repository**. Do not commit confidential, customer-specific, employer-specific, credential, personal, or otherwise non-public information.

AI agents modifying this repository **must** follow [`AI_RULES.md`](./AI_RULES.md). Security, public-repository safety, classification, and review rules are mandatory.

## Repository guide

- [`docs/philosophy.md`](./docs/philosophy.md) — design principles
- [`docs/architecture.md`](./docs/architecture.md) — conceptual model and AI selection flow
- [`docs/repository-structure.md`](./docs/repository-structure.md) — directory responsibilities
- [`docs/contribution.md`](./docs/contribution.md) — Issue/PR workflow
- [`AI_RULES.md`](./AI_RULES.md) — mandatory AI modification rules
- [`catalog/features.md`](./catalog/features.md) — feature catalog
- [`catalog/patterns.md`](./catalog/patterns.md) — reusable pattern catalog

## Current status

The repository structure and core rules are in place. The current focus is validating the full lifecycle with **Authentication** as the first proof of concept:

`Feature → Pattern → Standard → Template → Variant`

The feature catalog currently covers common application concerns such as Authentication, User, Authorization, CRUD, Form, Validation, Error Handling, API, Database, and File Upload. Additional features are intentionally staged for later expansion.

## Next focus

1. Complete the Authentication proof of concept.
2. Validate that each artifact is reusable and composable.
3. Add additional standards only after the lifecycle has been proven.
4. Improve AI-readable metadata and selection rules based on actual usage.
