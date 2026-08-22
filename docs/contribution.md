# Contribution and Change Flow

## Standard flow

`Issue → Design → Implementation → Validation → PR → Review → Merge`

## Issue types

- `[EPIC]` large initiative
- `[FEATURE]` capability definition
- `[PATTERN]` recognized solution pattern
- `[STANDARD]` reusable rule/constraint
- `[TEMPLATE]` concrete implementation artifact
- `[VARIANT]` controlled exception or extension
- `[SECURITY]` security-specific work
- `[TEST]` test/validation work
- `[AI]` AI discovery/selection/integration work
- `[DOCS]` documentation

## Required for non-trivial changes

1. Link the change to a GitHub Issue.
2. Identify the affected Feature/Pattern/Standard/Template/Variant.
3. Explain security and compatibility impact where applicable.
4. Update documentation/schema when the model changes.
5. Validate the change before merge.

## Promotion of a Variant

A Variant may be promoted when:

- the requirement is demonstrably reusable;
- the behavior can be described generically;
- security and compatibility implications are understood;
- it has sufficient validation or real usage evidence;
- the resulting Standard does not encode a customer/employer/project-specific detail.

## AI contribution rule

AI agents are welcome to implement issues, but must obey `AI_RULES.md`. In particular, an AI agent must not silently introduce confidential information, weaken security, bypass the Standardization Model, or turn project-specific requirements into public Standards.
