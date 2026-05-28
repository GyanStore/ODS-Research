# Assignment 1 — Problem formulation

**Author:** Shruthi Chinnasamy · PGD-AI, IIT Jodhpur · g25ait1165@iitj.ac.in

## Purpose

Define a rigorous optimization model for allocating 24 hours across six childhood activities (ages 3–6), suitable for classical solvers and later computational study.

## Files

| File | Description |
|------|-------------|
| [problem-formulation-linear-deviation.md](problem-formulation-linear-deviation.md) | **Primary Assignment 1 paper:** minimize \(\sum_i \|x_i - r_i\|\); auxiliary variables for LP; constraints from pediatric guidelines |
| [quadratic-programming-formulation-v3.md](quadratic-programming-formulation-v3.md) | **QP evolution:** maximize \(D = \sum w_i[-a_i(t_i-\mu_i)^2 + c_i]\); same six activities; test-case parameter tables |
| [problem-formulation.tex](problem-formulation.tex) | LaTeX source for IEEE-style submission |

## Six decision variables (Table 1)

| Variable | Activity | Domain |
|----------|----------|--------|
| \(t_1\) | Sleep | Physical health |
| \(t_2\) | Structured learning | Cognitive |
| \(t_3\) | Physical play | Motor skills |
| \(t_4\) | Creative play | Creativity |
| \(t_5\) | Meal times | Nutrition |
| \(t_6\) | Hygiene & chores | Life skills |

See [`../data/table1-activity-variables.csv`](../data/table1-activity-variables.csv).

## Constraint types

1. **Total time:** \(\sum t_i = 24\)
2. **Bounds:** \(L_i \le t_i \le U_i\) from AAP/WHO-style guidelines
3. **Logical links:** e.g., minimum sleep, meal windows (as specified in each document)

## Link to Assignment 2

The QP formulation in `quadratic-programming-formulation-v3.md` is the mathematical basis for the comparative methods paper in [`../assignment-02-comparative-optimization/`](../assignment-02-comparative-optimization/).
