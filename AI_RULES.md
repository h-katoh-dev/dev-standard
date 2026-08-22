# AI Modification Rules

> **This file defines mandatory rules for any AI agent modifying this repository.**

## 1. Absolute rules

1. **Do not add confidential or project-specific information.**
   - No customer names, internal URLs, credentials, secrets, API keys, personal data, proprietary source code, or non-public business rules.
   - The repository is public. Treat every committed file as publicly distributable.
2. **Do not weaken security standards for convenience.**
   - Authentication, authorization, password handling, session management, input validation, secrets handling, and similar areas must follow established security standards.
   - Never commit plaintext passwords, secrets, tokens, private keys, or credential examples that could be mistaken for real credentials.
3. **Do not silently change a Standard.**
   - Changes to a Standard require a GitHub Issue and reviewable PR.
   - Breaking changes must be explicitly identified and versioning impact documented.
4. **Do not turn a one-off implementation into a Standard without evidence.**
   - Project-specific or exceptional requirements belong under `variants/` until they meet the promotion criteria.
5. **Do not bypass the repository model.**
   - New reusable knowledge should be classified as Feature / Pattern / Standard / Template / Variant before implementation.
6. **Preserve technology independence where intended.**
   - Do not embed framework-specific assumptions into technology-neutral specifications.
   - Technology-specific implementations must be separated from the corresponding conceptual Standard.
7. **Update documentation and schemas when behavior or structure changes.**
8. **Prefer additive, backward-compatible changes.**
9. **Never delete or overwrite existing standards merely to make a task easier.**
10. **If a requested change conflicts with these rules, stop and raise the conflict in the GitHub Issue/PR instead of silently proceeding.**

## 2. Public repository rule

`dev-standard` is a public repository. Therefore:

- Only generic, reusable development knowledge may be committed.
- Real project information must be abstracted before inclusion.
- If information cannot be safely generalized, it must not be committed.
- AI agents must assume that all repository content will be publicly visible.

## 3. Change workflow

For non-trivial changes:

`Issue → Design → Implementation → Test/Validation → PR → Review → Merge`

AI may implement changes, but AI must not bypass the reviewable workflow for changes that affect standards, security, architecture, schemas, or reusable templates.

## 4. When uncertain

When the correct classification, security impact, compatibility impact, or public-safety of content is unclear, **do not guess**. Record the uncertainty and ask for a decision.
