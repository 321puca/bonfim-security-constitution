# Tree of Authority — Constitutional Governance Chain

This document defines the binding authority chain for all governance and security artifacts derived from this repository.

It expresses who (or what layer) can decide, amend, interpret, and operationalize security governance—while preserving Principle 01 (human accountability) and Article 01 (scope and authority).

## Authority Layers (Normative Order)

1. Constitution (this repository as the authoritative constitutional source)
2. Amendments (change control for the constitution itself)
3. Principles (immutable intent and interpretive anchors)
4. Articles (applicability, enforceable boundaries, and mandatory rules)
5. Derived Governance Artifacts (policies, standards, procedures, controls)
6. Decision Records (ADRs / decision-logs; traceability of choices)
7. Tabletop Exercises (TTX; validation by simulation)
8. Operational Implementations (code, configs, environments — explicitly out of scope here)

## Diagram (Authoritative)

```mermaid
flowchart TD
  A[Constitution<br/>Authoritative Source] --> B[Amendments<br/>Change Control]
  B --> C[Principles<br/>Immutable Intent]
  C --> D[Articles<br/>Enforceable Boundaries]
  D --> E[Derived Governance Artifacts<br/>Policies • Standards • Procedures • Controls]
  E --> F[Decision Records<br/>ADRs / Decision Logs]
  F --> G[Validation Artifacts<br/>TTX]
  G --> H[Operational Implementations<br/>Code • Config • Environments]

  %% Constraints
  C -. binds .-> D
  D -. governs .-> E
  A -. prevails .-> B

Binding Rules

Authority conflicts are resolved upward in the chain.

Articles and Principles override any derived artifact.

Amendments are additive and historically preserved; no overwrite is permitted.

Decision Records must explicitly reference the governing Principle(s) and/or Article(s).

No operational code, secrets, personal data, or environment-specific configuration may be committed to this repository.

Audit Trace Requirement

Any claim of compliance with this constitution must be traceable as follows:

Implementation → TTX Evidence → ADR Decision → Policy/Standard → Articles → Principles → Constitution.

Absence of this trace constitutes non-compliance, regardless of intent.
