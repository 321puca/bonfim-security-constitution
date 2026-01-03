# TTX Index — Tabletop Exercises Governance

## 1. Purpose

This document defines the authoritative framework for the creation, execution, validation, and archival of all Tabletop Exercises (TTX).

TTX are not simulations for training only.
They are governance instruments used to:

* Validate decision authority
* Expose risk ownership
* Test escalation paths
* Produce auditable evidence of preparedness

---

## 2. Scope

This framework applies to all TTX involving:

* Security incidents
* Privacy and GDPR scenarios
* Cloud and infrastructure failures
* AI-assisted decision systems
* Legal, reputational, or national-security-adjacent risks

No TTX exists outside this index.

---

## 3. Classification of TTX

Each TTX MUST be classified as one of the following:

* **TTX-SEC** — Security & Incident Response
* **TTX-GDPR** — Data Protection & Privacy
* **TTX-OPS** — Operational & Infrastructure
* **TTX-AI** — AI Governance & Automation Risk
* **TTX-STRAT** — Strategic / Cross-domain Governance

Hybrid exercises must declare a primary class.

---

## 4. Mandatory Structure of a TTX

Every TTX document MUST contain:

1. Scenario description
2. Trigger event
3. Assumptions
4. Roles and authority mapping
5. Decision points
6. Expected actions
7. Observability and evidence produced
8. Gaps identified
9. Risk ownership assignment
10. Post-exercise governance actions

Missing sections invalidate the TTX.

---

## 5. Authority and Participation

TTX participants must be explicitly authorized.

* Observers may not intervene
* Facilitators may not decide
* Decision-makers must act within documented authority

Authority conflicts are logged as governance failures.

---

## 6. Evidence and Auditability

Each TTX MUST generate:

* A timestamped record
* A written outcome
* A list of decisions taken
* Identified control failures
* Required follow-up actions

TTX outputs are immutable once finalized.

---

## 7. Storage and Versioning

TTX documents are stored under:

```
/ttx/
  ├─ index.md
  ├─ ttx-YYYY-MM-DD-<slug>.md
```

Edits require:

* New version
* Explicit rationale
* Reference to superseded version

---

## 8. Review Cycle

TTX relevance must be reviewed:

* Annually (minimum)
* After major incidents
* After regulatory or architectural changes

Stale TTXs are marked deprecated, never deleted.

---

## 9. Language and Authority

This document is authoritative in **English**.

Translations may exist but do not override this version.

---

## 10. Final Statement

TTX are not rehearsals.

They are **proof of governance under pressure**.
