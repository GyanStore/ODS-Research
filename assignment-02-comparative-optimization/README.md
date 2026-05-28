# Assignment 2 — Comparative optimization study

**Authors:** Shruthi Chinnasamy, Nishant Kumar · IIT Jodhpur  
**Emails:** g25ait1165@iitj.ac.in, nishantkumar@iitj.ac.in

## Purpose

Solve the childhood daily-routine QP with **empirically grounded** parameters and compare **Steepest Descent**, **Newton’s method**, **BFGS**, and **Conjugate Gradient** on three realistic scenarios.

## Main paper

[final-paper-comparative-optimization.md](final-paper-comparative-optimization.md) — full IEEE-style write-up: abstract, formulation, test cases, algorithms, results, deployment notes.

### Headline results

- **Best method:** BFGS (highest average developmental score, ~3.02 across cases).
- **Efficiency:** Often 2–5 iterations, ~0.003 s per problem instance.
- **Scenarios:** Standard weekday · Rainy day · Skill-focused day (parameters in [`../data/table2-test-case-parameters.csv`](../data/table2-test-case-parameters.csv)).

## Supporting materials

| Path | Description |
|------|-------------|
| [diagrams/flowchart-for-paper.md](diagrams/flowchart-for-paper.md) | Paper-ready flowchart narrative |
| [diagrams/flowchart-mermaid.md](diagrams/flowchart-mermaid.md) | Mermaid source for methodology figure |
| [diagrams/optimization-flowchart.svg](diagrams/optimization-flowchart.svg) | Vector methodology diagram |
| [diagrams/diagram-placeholders.md](diagrams/diagram-placeholders.md) | Figure slots for submission |
| [references/assignment-2-brief.pdf](references/assignment-2-brief.pdf) | Course assignment brief |
| [references/sample-best-assignment-2.pdf](references/sample-best-assignment-2.pdf) | Reference exemplar |

## Methods (overview)

| Method | Role in study |
|--------|----------------|
| Steepest Descent | Baseline first-order; slow on ill-conditioned QPs |
| Newton | Second-order; fast near optimum; Hessian cost |
| **BFGS** | Quasi-Newton; **recommended** balance of speed and cost |
| Conjugate Gradient | Low-memory; included for scalability perspective |

## Prerequisites

Read Assignment 1 QP formulation: [`../assignment-01-problem-formulation/quadratic-programming-formulation-v3.md`](../assignment-01-problem-formulation/quadratic-programming-formulation-v3.md).
