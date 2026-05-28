# Optimization Framework Flowchart
## For Early Childhood Daily Routine Problem

### Flowchart Logic Verification against ods-v3.md

**Paper Alignment Checklist:**
- ✅ Uses correct variable notation (tᵢ instead of rᵢ as per paper)
- ✅ References equation numbers from paper (Eq. 1-4)
- ✅ Includes all 6 activities from Table 1
- ✅ Shows quadratic objective function correctly
- ✅ Lists classical optimization methods mentioned in paper
- ✅ Emphasizes constraints from Section II.B
- ✅ Shows iterative refinement process
- ✅ Outputs complete optimal schedule

### Flowchart Structure:

```
START
  ↓
[INPUT PARAMETERS]
- Child age and developmental stage
- Activity weights (wᵢ)
- Ideal durations (μᵢ) from pediatric guidelines
- Penalty coefficients (aᵢ)
  ↓
[DEFINE CONSTRAINTS]
- Total time: Σtᵢ = 24 hours (Eq. 2)
- Activity bounds: Lᵢ ≤ tᵢ ≤ Uᵢ (Eq. 3)
- Meal structure: tB + tL + tD = t₅ (Eq. 4)
  ↓
[FORMULATE QUADRATIC OBJECTIVE]
- Maximize D = Σwᵢ[−aᵢ(tᵢ − μᵢ)² + cᵢ] (Eq. 1)
- Subject to defined constraints
  ↓
[APPLY CLASSICAL OPTIMIZATION]
- Sequential Quadratic Programming (SQP)
- Newton/Quasi-Newton methods
- Gradient-based approaches
  ↓
[COMPUTE OPTIMAL ALLOCATION]
- Find optimal time allocation t*ᵢ
- For each activity (i = 1, 2, ..., 6)
  ↓
<DECISION: All Constraints Satisfied?>
  No → [Loop back to Apply Optimization]
  Yes ↓
[OPTIMAL DAILY SCHEDULE]
- Sleep: t*₁ hours | Learning: t*₂ hours
- Physical Play: t*₃ hours | Creative Play: t*₄ hours
- Meals: t*₅ hours | Hygiene: t*₆ hours
- with Σt*ᵢ = 24 hours
  ↓
[DEVELOPMENTAL SCORE]
- D* = Σwᵢ[−aᵢ(t*ᵢ − μᵢ)² + cᵢ]
  ↓
END
```

### Key Improvements Made:

1. **Corrected Variable Notation:** Changed rᵢ to tᵢ throughout (paper uses tᵢ for time allocation)

2. **Added Equation References:** Linked each step to specific equations in the paper

3. **Complete Activity List:** Shows all 6 activities explicitly in output

4. **Proper Mathematical Notation:** Used correct subscripts and Greek letters

5. **Classical Methods Focus:** Emphasized SQP, Newton methods, and gradient-based approaches (as stated in paper)

6. **Clearer Logic Flow:** Better organized constraint definition and objective formulation

7. **Professional Styling:** IEEE-appropriate colors and clean typography

8. **Developmental Context:** Added child age/stage input to match paper's focus

### Color Coding:
- **Blue (Input):** Parameter inputs
- **Orange (Input Box):** Initial data entry
- **Purple (Process):** Mathematical formulation and computation steps
- **Yellow (Decision):** Constraint validation decision point
- **Green (Output):** Final results and scores

### Usage Instructions:
1. **For Word/DOCX:** Copy the SVG code and paste into Word, or insert as image
2. **For LaTeX:** Use `\includegraphics{optimization_flowchart.svg}` or convert to PDF
3. **For Presentations:** Export as PNG or use SVG directly
4. **For IEEE Paper:** Caption as "Fig. 1. Flowchart of the optimization process..."

### Recommended Caption:
**Fig. 1.** Flowchart of the early childhood routine optimization process, showing input parameters, constraint processing, quadratic objective formulation, classical optimization methods, and output generation of an optimal daily schedule with developmental score.
