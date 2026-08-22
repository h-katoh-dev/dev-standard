# Dev Standard Philosophy

## Purpose

`dev-standard` is a public, reusable development standard for reducing repeated design and implementation work in applications and web systems.

The goal is not merely to store code snippets. The goal is to make recurring engineering decisions explicit, reusable, testable, and eventually selectable by AI through structured dialogue.

## Core principles

### 1. Standardize decisions before code

A reusable implementation is valuable, but a reusable decision model is more valuable. Define what the feature must do, which patterns are supported, and what quality/security requirements apply before creating implementation templates.

### 2. Standard first, exception second

Common requirements should become Standards. Exceptional requirements should remain Variants until their reuse and generality justify promotion.

### 3. Public by default

This repository is public. Only generalized, reusable knowledge belongs here. Customer, employer, project, credential, personal, or otherwise confidential information must never be committed.

See `AI_RULES.md` for mandatory rules for AI-assisted modification.

### 4. Security is part of the Standard

Security is not an optional afterthought for security-sensitive features. Password handling, authorization, session management, validation, secrets, logging, and related controls must be represented explicitly in the relevant Standard.

### 5. Technology-neutral specification where possible

The conceptual Standard should remain independent of a specific framework when practical. Technology-specific Templates implement that Standard for a concrete stack.

### 6. Variants are learning mechanisms

A Variant is not a failure of standardization. It is a controlled way to capture exceptional requirements. Repeated and generalized Variants can be promoted into new Patterns or Standards.

### 7. Machine-readable from the beginning

Human-readable Markdown remains important, but definitions should eventually have machine-readable schemas so an AI agent can discover, compare, validate, and select them reliably.

### 8. Reproducibility over cleverness

A Standard should be understandable and reproducible by another engineer or AI agent. Prefer explicit conventions over implicit knowledge.

## Standardization lifecycle

`Real requirement → Feature → Pattern → Standard → Template → Variant feedback → Standard evolution`

The lifecycle is iterative. Standards are versioned knowledge, not immutable doctrine.

## Definition of a good Standard

A Standard should answer, at minimum:

- What problem does it solve?
- When should it be used?
- What is required?
- What is optional?
- What security controls apply?
- What inputs/outputs/contracts exist?
- What tests are expected?
- What technology-neutral constraints exist?
- Which implementation Templates are available?
- What known Variants exist?
- What are the compatibility and versioning implications?
