# ADR-SEC-001 — API Key Management and Secret Handling

## Status

Accepted

---

## Context

During routine operations and subsequent investigation, an API key used for AI-assisted services was suspected to have been exposed through local shell configuration and tooling misalignment.

The incident was formally analyzed and documented under **TTX-SEC-2026-01**, which identified systemic weaknesses in secret handling, rotation, and local environment isolation.

The organization operates under strict requirements of:

* SecOps
* GDPR
* Security-by-design
* Auditability
* National and organizational security responsibility

Continuing without architectural correction would constitute an unacceptable governance risk.

---

## Decision

The organization adopts the following binding architectural decisions:

1. **Plaintext API keys are prohibited** in:

   * Shell configuration files (`.zshrc`, `.bashrc`, `.profile`)
   * Source code
   * Scripts
   * CI/CD configuration files without secret managers

2. **All API keys and secrets must be stored in a secure secret manager**, with macOS Keychain approved for local development environments.

3. **Runtime loading of secrets** must occur via:

   * Explicit secure loaders
   * Environment-scoped injection
   * Non-persistent memory whenever possible

4. **API key rotation is mandatory** after:

   * Any suspected exposure
   * Any configuration drift
   * Any environment rebuild

5. **Logs and artifacts must never contain secrets**, even partially.

---

## Consequences

### Positive

* Reduced blast radius of secret exposure
* Clear audit trail for incident response
* Alignment with GDPR data minimization and security principles
* Professional-grade security posture suitable for regulated environments

### Negative / Trade-offs

* Slight increase in setup complexity for developers
* Requirement for onboarding documentation and tooling discipline

These trade-offs are accepted as necessary for security maturity.

---

## Compliance and Governance Alignment

This decision enforces and derives authority from:

* Organizational Constitution
* Governance Principles
* TTX-SEC-2026-01 findings

Non-compliance with this ADR constitutes:

* A governance violation
* A security incident
* A reviewable disciplinary or corrective action

---

## Implementation Notes

* macOS Keychain is the approved local secret store
* Future extensions may include:

  * Vault-based secret management
  * Cloud-native secret managers
  * Automated rotation policies

---

## Review Cycle

This ADR must be reviewed:

* Annually, or
* After any secret-related incident, whichever occurs first

---

## Final Statement

Secrets are not configuration details.

They are **security assets**.

Their governance is non-negotiable.

