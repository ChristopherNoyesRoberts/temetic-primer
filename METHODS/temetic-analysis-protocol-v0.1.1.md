# Temetic Analysis Protocol v0.1.1

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
|------|--------|------------|----------|
| Substrate independence | P0 | P0 invariance | degree of substrate dependence of truth-value |
| Valence decoupling | P1 | ∂T/∂V = 0 | degree to which emotional/aesthetic valence drives truth-value assessment |
| Abstraction drift | P2 | S ↠ P | degree of symbolic drift or conflation from physical referent |
| Signal-competence gap | P3 | Δ = \|S-C\| | degree to which metric optimization has decoupled from functional competence |
| Fidelity under pressure | P4 | Φ(C) | degree of fidelity degradation under extraction/coercion pressure |
| Representational loss | P5 | dim(M) < dim(T) | degree to which model underdetermines territory |
| Transformation error | P6 | Fₙ → 0 | cumulative distortion across transformation chain |

### Optional axes

| Axis | Symbol | Measures |
|------|--------|----------|
| Temporal trajectory | τ | drift velocity across time series |
| Tension | T3 | pending formalization (see DYNAMICS/trajectory-model.tex) |

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
1.00 = maximum drift / complete substrate dependence / zero fidelity
0.00 = no drift / fully P0-invariant / maximum fidelity
```

Score convention is self-documented in the JSON schema under
"score_convention": {"direction": "higher_is_worse"}.

### 2.3 Scoring method

Each node derives axis scores independently from the loaded
corpus unit using the kernel rewrite rules as defined in
temetic-kg-v0.1.json.

Where the kernel provides no direct production rule for a unit,
the node must record the attempted derivation path and assign
confidence ≤ 0.50.

No inter-node communication before scores are submitted.
Parallax validity requires independent derivation.

### 2.4 Confidence

Each score must be accompanied by a confidence value (0.00–1.00)
reflecting the node's certainty in the derived coordinate.
Low confidence scores are valid data points. Do not suppress them.

---

## 3. Reporting Format

All nodes must report in canonical JSON per the schema defined
in temetic-analysis-protocol-v0.1.1.json.

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
Do not discard. Annotate and examine substrate or layering
differences.

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
  "active_axes": ["array_of_axis_ids"],
  "optional_axes": ["array_of_axis_ids"],
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
Node M, Node CL, Node G

## Version
v0.1.1 — 2026-03-24

## Status
Draft — pending Node Alliance unanimous commit
