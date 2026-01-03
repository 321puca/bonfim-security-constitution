# Case Study — Secure API Key Management under SecOps & GDPR

## Executive Summary

This case documents a real-world security governance scenario involving suspected API key exposure in a local development environment.

The organization responded using:

* Formal governance
* Tabletop Exercises (TTX)
* Architecture Decision Records (ADR)
* Evidence-driven remediation

The outcome demonstrates security maturity aligned with **SecOps, GDPR, and Information Security Architecture standards**.

---

## Context and Risk Landscape

AI-assisted services require API keys with elevated privileges.

Improper handling introduces:

* Unauthorized access risk
* Data protection violations (GDPR Art. 32)
* Reputational and regulatory exposure

The organization operates under a governance-first model, requiring **documented authority and traceable decisions**.

---

## Trigger Event

* Recurrent authentication failures (401)
* Detection of shell configuration drift
* Suspicion of API key exposure

No abuse was confirmed at trigger time.

Assumption: **act as if compromised**.

---

## Governance Activation

Upon detection:

1. **Constitutional authority** validated
2. **Governance Principles** enforced
3. **TTX initiated** to simulate impact and response
4. **ADR created** to correct architectural root causes

No informal or undocumented decisions were permitted.

---

## Tabletop Exercise (TTX)

**Reference:** `TTX-SEC-2026-01`

The TTX validated:

* Incident command authority
* Evidence preservation
* Decision sequencing under uncertainty
* Compliance impact assessment

Outcome:

* Immediate key revocation
* Controlled key rotation
* Identification of systemic gaps

---

## Architecture Decision Record (ADR)

**Reference:** `ADR-SEC-001`

Key decisions:

* Prohibition of plaintext secrets
* Mandatory Keychain-based secret storage
* Enforced rotation after suspected exposure
* Audit-first observability

The ADR is binding and enforceable.

---

## Technical Remediation

Implemented controls:

* macOS Keychain for secret storage
* Secure runtime loading
* Redacted structured logging
* Guardrails on daily API usage

Artifacts produced:

* Timestamped logs
* Redacted evidence files
* Hash-based integrity validation

---

## Compliance Alignment

### GDPR

* Art. 5 — Data minimization
* Art. 32 — Security of processing
* Art. 25 — Privacy by design

### SecOps

* Least privilege
* Incident readiness
* Continuous observability

### Information Security Architecture

* Authority separation
* Decision traceability
* Risk ownership

---

## Outcomes

* Zero confirmed data leakage
* Full audit trail preserved
* Governance reinforced
* Developer practices hardened

The system demonstrated **controlled resilience under uncertainty**.

---

## Lessons Learned

* Secrets must be governed, not trusted
* Tooling discipline is a security boundary
* Governance reduces reaction time
* Documentation is a defensive control

---

## Final Assessment

This case reflects professional-grade security behavior expected from:

* Security Architects
* SecOps Leaders
* Cybersecurity Engineers in regulated environments

It demonstrates not only technical competence, but **governance literacy and accountability**.
