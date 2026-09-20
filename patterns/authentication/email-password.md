# Email + Password Authentication Pattern

## Purpose

Provide a common authentication approach using an email address and password as the primary user credentials.

This is a technology-neutral Pattern. Framework-specific implementation details belong in Templates.

## When to use

Use this Pattern when:

- users need account-based sign-in with an email address;
- password-based authentication is an accepted user experience;
- the selected technology stack provides a secure credential and session mechanism.

Do not select this Pattern when passwordless or federated authentication is a required primary flow. Consider Passkey or OAuth instead.

## Core flow

1. User submits an email address and password.
2. The system validates the request.
3. The system verifies the credentials using a secure password-verification mechanism.
4. On success, the system establishes an authenticated session.
5. On failure, the system returns a generic authentication failure without exposing credential-specific details.

## Security expectations

Implementations of this Pattern must:

- never store plaintext passwords;
- use a password-hashing mechanism designed for password storage;
- protect authentication endpoints against abuse and excessive attempts;
- protect authenticated sessions according to the selected platform's security model;
- keep secrets and credentials outside source control;
- avoid revealing whether an account exists through unnecessary response differences;
- define password reset and email verification behavior when those capabilities are required.

Detailed security requirements belong in the applicable Standards.

## Boundaries

This Pattern does not define:

- a specific framework or programming language;
- a specific password-hashing library;
- a specific session/token technology;
- UI design;
- deployment infrastructure.

Those decisions belong to Standards, Templates, or Variants as appropriate.

## Related patterns

- OAuth
- Passkey
- MFA / 2FA
- Email Verification
- Password Reset
- Session Management
- Login Attempt Control

## Template relationship

A technology-specific Template implementing this Pattern must identify:

- the supported stack and version assumptions;
- the applicable Standards;
- required dependencies or platform services;
- implementation and test expectations.
