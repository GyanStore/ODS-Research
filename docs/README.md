# Documentation index

## Assignments (IIT Jodhpur — Optimization of Data Science)

### Assignment 1 — Problem formulation

- **Goal:** Cast early-childhood daily scheduling as a constrained optimization problem.
- **First model:** Minimize total deviation from recommended hours using absolute values; LP reformulation with \(d_i^+, d_i^-\).
- **Evolved model (v3):** Maximize quadratic Daily Developmental Score with ideal durations and penalties.
- **Files:** [`../assignment-01-problem-formulation/`](../assignment-01-problem-formulation/)

### Assignment 2 — Comparative optimization

- **Goal:** Implement and compare four classical methods on three empirically parameterized test cases.
- **Methods:** Steepest Descent, Newton, BFGS, Conjugate Gradient.
- **Outcome:** BFGS recommended for speed, stability, and score.
- **Files:** [`../assignment-02-comparative-optimization/`](../assignment-02-comparative-optimization/)

## Data & diagrams

- **Parameters:** [`../data/`](../data/) — CSV tables + Table II guide.
- **Flowcharts:** [`../diagrams/`](../diagrams/) and Assignment 2 [`../assignment-02-comparative-optimization/diagrams/`](../assignment-02-comparative-optimization/diagrams/).

## Empirical sources (cited in papers)

- **CDS** — Child Development Supplement, time-use (2,500+ children).
- **WHO** — Physical activity / sleep meta-analyses (69,542 children, 18 countries).
- **MICS** — UNICEF Multiple Indicator Cluster Surveys (116+ countries).

## Formulation notation (quick reference)

| Symbol | Meaning |
|--------|---------|
| \(t_i\) | Hours allocated to activity \(i\) |
| \(w_i\) | Importance weight (dimensionless) |
| \(\mu_i\) | Ideal duration (hours) |
| \(a_i\) | Quadratic penalty (1/hours²) |
| \(L_i, U_i\) | Lower / upper bounds (hours) |
| \(D\) | Daily Developmental Score |
