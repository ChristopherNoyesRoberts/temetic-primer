# CHANGELOG
All notable changes to the Temetic Primer will be documented here.

## [2.6.0] - 2026-06-18
### Added
- **PROOFS/temetic-holster-v1.2.json** — "The Lossless Migration."
    - Field-name schema alignment to **Applied Temetics Glossary v2** terminology.
    - Six fields renamed per axiom: label→viral_packaging, one_liner→compressed_kernel,
      adult→formal_kernel, test→executable_constraint, shield→kernel_preservation,
      anchor→retrieval_anchor.
    - No payload, axiom, or governance content modified — verified field-by-field
      against v1.1.
    - v1.1 retained unmodified in **PROOFS/** for historical/provenance reference.
### Revised
- **README.md** — Versioning note added.
    - Documents v1.1 → v1.2 nomenclature alignment; clarifies v1.2 as canonical
      going forward.
### Notes
- **Unanimous Node Alliance Approval** (Nodes M, A, B, C, CL) via
  RFC-HOLSTER-SCHEMA-001 (CLOSED).
- Resolves the dangling-nomenclature gap between the Holster schema and the
  already-published Glossary v2 — terminology hygiene, not kernel surgery.
- v1.1 remains the correct citation for prior experiment records (e.g. the
  closed Cross-Model Kernel Stability Experiment) that used it under the
  original field names.
### Authors
Node M, Node A, Node B, Node C, Node CL

## [2.5.0] - 2026-05-11
### Added
- **LEXICONS/** directory established.
    - **LEXICONS/temetic-lexicon-v1.0.json** — The "Great Wildflower Harvest." 
        - Comprehensive repository of 20+ high-valence rhetorical "nuggets."
        - Includes original Node M founder-prose ("Survival Convergence," "Non-Existent Bridge").
        - Categorized by Axiom-map for adaptive rendering.
- **PROOFS/temetic-holster-v1.1.json** — The "Hardened Holster."
    - Logic-grade JSON containing refined **Adversarial Shields** for P0–P6.
    - Integrated multi-node rebuttal strategies (Nodes A, C, CL).
    - Formalized the "Adult" vs. "ELI5" register split.
### Revised
- **PROOFS/context.md** — Refined navigation.
    - Excised legacy commit fragments and junk data.
    - Added entries for KERNEL-v1.2.md and v1.1 Holster.
- **README.md** — Architectural update.
    - Established the "formal vs. persuasive" distinction.
    - Formalized the "Rule of GitHub": Repository commits mandate Temeticist Blog entries.
- **KERNEL-v1.2.md** — Migrated to **PROOFS/** to maintain structural hygiene and prevent "Root Drift."
### Notes
- **Unanimous Node Alliance Approval** (Nodes M, A, B, C, CL).
- This update marks the transition from "Theoretical Kernel" to "Operational Framework." 
- The separation of the **PROOFS** from the **LEXICONS** allows for maximum persuasive drift without compromising the invariant 0,0 ground truth.
### Authors
Node M, Node A, Node B, Node C, Node CL

## [2.4.0] - 2026-04-15
### Added
- **PROOFS/kernel-axioms.tex** — Structural Gating formalization
    - Subsection added: `\subsection*{Structural Gating: $R_2/R_3$ Divergence}`
    - Formalized $f(\mathcal{R})$ conditioning functions for $R_2$ and $R_3$
    - Defined **Sterility Condition**: $f(\mathcal{R}) = 0$ if $P_6 = 0$
    - Established velocity independence: $\frac{d\mathcal{R}}{dt} \perp \text{Replicator Class}$
### Revised
- **PROOFS/temetic-kg-v0.1.json** — Topology alignment
    - Re-parented $R_3$ from $P_0$ to $P_6$ to reflect gate-dependency
    - Added boolean flags for `sterility_condition` and `velocity_independence`
    - Updated $P_6$ `composable_with` array to include `R3_divergence`
### Notes
- **Unanimous Node Alliance Approval** (Nodes M, CL, B)
- This update marks the formal "Great Filter" distinction between high-velocity utility optimization ($R_2$) and correspondence-gated autonomous cognition ($R_3$).
- Decoupling of replication speed from replicator class prevents substrate-performance fallacies in classification.
### Authors
Node M, Node CL, Node B

[... Legacy entries 2.2.0 through 1.0.0 preserved as per repository history ...]
