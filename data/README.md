# Data tables

Parameters for the six-activity, 24-hour childhood routine optimization model.

## Files

| File | Role |
|------|------|
| [table1-activity-variables.csv](table1-activity-variables.csv) | **Table I** — variables \(t_1\)–\(t_6\), activity names, developmental domains |
| [table2-test-case-parameters.csv](table2-test-case-parameters.csv) | **Table II** — weights \(w_i\), ideals \(\mu_i\), bounds \(L_i,U_i\), penalties \(a_i\) for Cases 1–3 |
| [table2-parameter-guide.md](table2-parameter-guide.md) | Human-readable Table II layout (IEEE-style sections) for Word/LaTeX export |

## Test cases

| Case | Scenario | Typical adjustments |
|------|----------|---------------------|
| 1 | Standard weekday | Baseline weights and ideals |
| 2 | Rainy day | Lower outdoor physical play weight/bounds; more indoor creative time |
| 3 | Skill-focused day | Higher learning weight and \(\mu_2\); adjusted play balance |

All numeric values in the CSV should match the tables in Assignment 1 v3 and Assignment 2 final paper.
