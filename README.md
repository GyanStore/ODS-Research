# ODS-Research

**Optimization of Data Science — Child development**

Mathematical optimization of balanced daily routines for early childhood (ages 3–6): problem formulation, empirically grounded parameters, and a comparative study of classical numerical methods.

**Authors:** Shruthi Chinnasamy (PGD-AI, IIT Jodhpur), Nishant Kumar (Electrical Engineering, IIT Jodhpur)  
**Contact:** g25ait1165@iitj.ac.in, nishantkumar@iitj.ac.in  
**Course context:** PG Diploma in Artificial Intelligence, IIT Jodhpur — Optimization of Data Science assignments

---

## Research arc

| Phase | Focus | Location |
|-------|--------|----------|
| **Assignment 1** | Problem formulation — LP deviation minimization → QP developmental score | [`assignment-01-problem-formulation/`](assignment-01-problem-formulation/) |
| **Assignment 2** | Computational study — BFGS, Newton, Steepest Descent, Conjugate Gradient on three test cases | [`assignment-02-comparative-optimization/`](assignment-02-comparative-optimization/) |

**Formulation evolution:** linear absolute-deviation minimization (Assignment 1) → concave quadratic **Daily Developmental Score** with ideal durations μᵢ and penalty coefficients aᵢ (v3 QP, used in Assignment 2).

---

## Problem (summary)

**Decision variables:** \(t_1,\ldots,t_6\) — hours per day for sleep, structured learning, physical play, creative play, meals, hygiene/chores.

**Objective (QP, Assignment 2):**

\[
\text{Maximize } D = \sum_{i=1}^{6} w_i \left[-a_i(t_i - \mu_i)^2 + c_i\right]
\]

Concave quadratics model diminishing returns around evidence-based ideal durations.

**Constraints (typical):**

- \(\sum_i t_i = 24\) (total day)
- \(L_i \le t_i \le U_i\) (pediatric bounds)
- Logical / scenario-specific constraints (e.g., rainy-day outdoor limits)

**Data grounding:** parameters tied to CDS time-use surveys (2,500+ children), WHO meta-analyses (69,542 children, 18 countries), and MICS (116+ countries) — not synthetic-only benchmarks.

**Test cases (Table 2):**

1. **Case 1 — Standard weekday**  
2. **Case 2 — Rainy day** (reduced outdoor physical play)  
3. **Case 3 — Skill-focused day** (emphasis on structured learning)

**Methods compared (Assignment 2):** Steepest Descent, Newton’s method, BFGS, Conjugate Gradient. **Main result:** BFGS achieves best average developmental scores (~3.02), typically 2–5 iterations and ~0.003 s per solve.

---

## Repository layout

```
├── README.md
├── docs/README.md
├── assignment-01-problem-formulation/   # Formulation papers (LP → QP)
├── assignment-02-comparative-optimization/  # Full comparative paper + diagrams + brief PDFs
├── data/                                # Table 1 (activities), Table 2 (case parameters)
└── diagrams/                            # Framework flowcharts (Assignment 1 / global)
```

---

## Key documents

| Document | Description |
|----------|-------------|
| [problem-formulation-linear-deviation.md](assignment-01-problem-formulation/problem-formulation-linear-deviation.md) | Assignment 1: minimize \(\sum \|x_i - r_i\|\) with LP reformulation |
| [quadratic-programming-formulation-v3.md](assignment-01-problem-formulation/quadratic-programming-formulation-v3.md) | QP developmental score formulation (v3) |
| [problem-formulation.tex](assignment-01-problem-formulation/problem-formulation.tex) | LaTeX source (Assignment 1) |
| [final-paper-comparative-optimization.md](assignment-02-comparative-optimization/final-paper-comparative-optimization.md) | Assignment 2: methods, experiments, conclusions |
| [table1-activity-variables.csv](data/table1-activity-variables.csv) | Six activities and developmental domains |
| [table2-test-case-parameters.csv](data/table2-test-case-parameters.csv) | Weights, ideals, bounds, penalties for Cases 1–3 |
| [table2-parameter-guide.md](data/table2-parameter-guide.md) | Complete Table II structure for papers |

---

## Branches

| Branch | Contents |
|--------|----------|
| `main` | Full curated documentation set |
| `assignment-01-problem-formulation` | Assignment 1 only |
| `assignment-02-comparative-optimization` | Assignment 2 only |
| `research/v1.0` | Frozen snapshot tag for citations |

---

## Related work

- **NeuroVal** — evaluation / sheaf-topology framework for LLMs (separate repo)  
- **Qualia** — CQTNN architecture and metric-driven frameworks (separate repo)

---

## License

Academic research output from IIT Jodhpur coursework. Contact authors for reuse beyond citation.
