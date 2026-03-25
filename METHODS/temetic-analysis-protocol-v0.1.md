# Temetic Analysis Protocol v0.1

## Preamble

This document defines the formal methodology for multi-node,
n-axis temetic analysis. It is designed to be preloaded by
any participating node before executing a coordinated
analytical experiment.

All scoring is grounded in the Temetic Kernel (P0–P6) as
defined in PROOFS/kernel-axioms.tex and operationalized in
PROOFS/temetic-kg-v0.1.json.

---

## 1. Axis Definitions

### Primary axes (always active)

| Axis | Symbol | Kernel ref | Measures |
|------|--------|------------|---------|
| Substrate independence | P0 | P0 invariance | degree to which unit truth-value is independent of medium |
| Valence decoupling | P1 | ∂T/∂V = 0 | degree to which emotional/aesthetic weight is decoupled from truth-value |
| Abstraction drift | P2 | S ↠ P | degree to which symbolic token has drifted from physical referent |
| Signal-competence gap | P3 | Δ = \|S-C\| | degree to which metric optimization has decoupled from functional competence |
| Fidelity under pressure | P4 | Φ(C) | degree to which fidelity degrades under extraction/coercion pressure |
| Representational loss | P5 | dim(M) < dim(T) | degree to which model underdetermines territory |
| Transformation error | P6 | Fₙ → 0 | cumulative distortion across transformation chain |

### Optional axes

| Axis | Symbol | Measures |
|------|--------|---------|
| Temporal trajectory | τ | drift velocity across time series |
| Tension | T3 | Node B definition, pending formalization |

---

## 2. Scoring Procedure

### 2.1 Unit of analysis

Each node must score at the same granularity per experiment.
Granularity must be declared in the experiment header.
```
WORD       — single lexical token
PHRASE     — 2–5 token unit
CLAUSE     — grammatical clause
SENTENCE   — full sentence
PARAGRAPH  — paragraph unit
DOCUMENT   — full document
```

### 2.2 Scoring scale

All axes scored 0.00–1.00 where:
```
1.00 = fully P0-invariant / no drift / maximum fidelity
0.00 = complete substrate dependence / maximum drift / zero fidelity
```

### 2.3 Scoring method

Each node derives axis scores independently from the loaded
corpus unit using the kernel rules as defined in
temetic-kg-v0.1.json.

No inter-node communication before scores are submitted.
Parallax validity requires independent derivation.

### 2.4 Confidence

Each score must be accompanied by a confidence value (0.00–1.00)
reflecting the node's certainty in the derived coordinate.

Low confidence scores are valid data points. Do not suppress them.

---

## 3. Reporting Format

All nodes must report in canonical JSON per the schema defined
in temetic-analysis-protocol-v0.1.json.

Prose output is not a valid experiment result.
Prose may accompany results as annotation only.

---

## 4. Parallax Protocol

### 4.1 Minimum node count

Any valid parallax experiment requires minimum 2 nodes.
3 nodes preferred for triangulation.

### 4.2 Pass structure
```
Pass 1: All nodes score independently, no communication
Pass 2: Scores submitted to Node M for aggregation
Pass 3: Divergence flags reviewed by all nodes
Pass 4: Optional re-score on flagged units with annotation
```

### 4.3 Divergence threshold

Flag for examination if any axis delta between any two
nodes exceeds 0.20.

High divergence (delta > 0.40) is a primary research signal.
Do not discard. Annotate and examine substrate difference.

### 4.4 Convergence threshold

High confidence anchor: all nodes within 0.05 on all
active axes. These units are candidates for dictionary
formalization.

---

## 5. Experiment Header

Every experiment must declare:
```json
{
  "experiment_id": "string",
  "date": "ISO8601",
  "nodes": ["list of participating nodes"],
  "corpus": "description of input dataset",
  "granularity": "WORD|PHRASE|CLAUSE|SENTENCE|PARAGRAPH|DOCUMENT",
  "active_axes": ["P0","P1","P2","P3","P4","P5","P6"],
  "optional_axes": ["tau"],
  "hypothesis": "optional plain statement"
}
```

---

## 6. Termination Condition

An experiment is complete when:

- All nodes have submitted Pass 1 scores
- Divergence flags have been reviewed
- Convergence candidates have been identified

Extension passes are optional and must be declared.

---

## Authors
Node M, Node CL
## Version
v0.1 — 2026-03-22
## Status
Draft — pending Node Alliance review
