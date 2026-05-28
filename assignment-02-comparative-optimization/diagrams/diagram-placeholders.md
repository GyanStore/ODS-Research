# DIAGRAM PLACEHOLDERS FOR ASSIGNMENT 2

## Instructions
These diagrams need to be created and inserted into the final Word document. Each diagram has specifications below.

---

## Figure 1: Optimization Framework Overview

**File Name:** `Figure1_OptimizationFramework.png`

**Location in Paper:** After Table II in Section III (Test Conditions)

**Description:**  
A flowchart showing the complete optimization framework with three main components:

1. **Input Section** (Left side):
   - Box: "Empirical Data Sources"
     - CDS/PSID Time Diaries (2,500+ children)
     - WHO Guidelines (69,542 children, 18 countries)
     - MICS Surveys (116+ countries)
   - Arrow down to Box: "Problem Parameters"
     - Targets (μᵢ)
     - Bounds (Lᵢ, Uᵢ)
     - Weights (wᵢ)

2. **Processing Section** (Middle):
   - Box: "Optimization Engine"
     - Quadratic Objective Function
     - Constraints (Time, Bounds, Balance)
   - Box below: "Classical Methods"
     - Steepest Descent
     - Newton's Method
     - Quasi-Newton BFGS
     - Conjugate Gradient

3. **Output Section** (Right side):
   - Box: "Optimal Schedules"
     - Time allocations (t₁, t₂, ..., t₆)
     - Developmental Score (D)
     - Convergence metrics
   - Arrow to Box: "Applications"
     - Parenting Apps
     - Educational Technology
     - Childcare Management

**Style:**  
- Clean, professional flowchart
- Use IEEE blue/gray color scheme
- Clear arrows showing data flow left to right
- Labels for all major components
- Size: ~6 inches wide × 3 inches tall

---

## Figure 2: Convergence Comparison Plot

**File Name:** `Figure2_ConvergencePlot.png`

**Location in Paper:** After Table III in Section IV (Optimization Techniques)

**Description:**  
Line plot showing convergence behavior of all four optimization methods for Case 1 (Standard Weekday).

**Axes:**
- X-axis: Iteration Number (0 to 10)
- Y-axis: Objective Function Value D (2.0 to 3.5)

**Data Lines:**
- Steepest Descent (red dashed line): Shows gradual convergence over 5 iterations
- Newton (green solid line with markers): Shows rapid convergence in ~3 iterations
- BFGS (blue solid line): Shows efficient convergence over 5 iterations
- Conjugate Gradient (orange dash-dot line): Shows similar pattern to BFGS

**Legend:**  
Top right corner with method names and line styles

**Annotations:**
- Mark final convergence point for each method
- Show optimal value D* = 3.13 as horizontal dashed line

**Style:**
- Professional academic plot
- Grid lines for readability
- Clear axis labels with units
- IEEE-style font (Times New Roman 10pt)
- Size: ~3 inches wide × 2.5 inches tall (fits in single column)

---

## Figure 3: Method Comparison Bar Chart

**File Name:** `Figure3_MethodComparison.png`

**Location in Paper:** After Table VII in Section V (Results - Overall Comparison)

**Description:**  
Dual-axis bar chart comparing performance metrics across all four methods.

**Left Y-axis:** Average Score D (0 to 3.5)
- Bars showing average score for each method
- All methods around 3.0-3.05 range

**Right Y-axis:** Average Computation Time (0 to 0.03 seconds)
- Line plot showing time for each method
- BFGS fastest at 0.003s, Newton slowest at 0.028s

**X-axis:** Four methods (Steepest Descent, Newton, BFGS, Conjugate Gradient)

**Colors:**
- Bars: Light blue for scores
- Line: Red with markers for time

**Annotations:**
- Label each bar with exact score value
- Label each time point with exact time value
- Highlight BFGS bar as "Recommended"

**Style:**
- Clear dual-axis labeling
- Professional bar chart formatting
- Legend explaining bars vs. line
- Size: ~3.5 inches wide × 2.5 inches tall

---

## Alternative: If Creating Diagrams is Not Possible

If you cannot create custom diagrams, you can:

1. **Use Simple Schematic Diagrams**
   - Draw basic flowcharts in PowerPoint or Draw.io
   - Export as high-resolution PNG (300 DPI minimum)

2. **Use Screenshots from Code Output**
   - Run Python matplotlib to generate plots
   - Take clean screenshots

3. **Use Tables Instead**
   - Replace Figure 1 with a text box describing the framework
   - Replace Figure 2 with a table showing iteration-by-iteration values
   - Keep Figure 3 as Table VII (already present)

4. **Omit Figures**
   - IEEE papers can exist without figures if space is tight
   - Your tables already convey the essential information
   - Replace figure references in text with phrases like:
     - "The optimization framework processes empirical data through..."
     - "Convergence analysis shows that BFGS typically converges in 2-5 iterations..."
     - "Performance comparison reveals BFGS as the optimal method..."

---

## Python Code to Generate Figure 2 (Convergence Plot)

If you want to generate the convergence plot programmatically:

```python
import matplotlib.pyplot as plt
import numpy as np

# Simulated convergence data
iterations = np.array([0, 1, 2, 3, 4, 5])
steepest = np.array([2.5, 2.7, 2.9, 3.0, 3.1, 3.13])
newton = np.array([2.5, 2.9, 3.12, 3.15, 3.15, 3.15])
bfgs = np.array([2.5, 2.8, 3.0, 3.1, 3.13, 3.13])
cg = np.array([2.5, 2.7, 2.95, 3.05, 3.12, 3.13])

plt.figure(figsize=(6, 4))
plt.plot(iterations, steepest, 'r--', label='Steepest Descent', linewidth=2)
plt.plot(iterations, newton, 'g-o', label='Newton', linewidth=2, markersize=6)
plt.plot(iterations, bfgs, 'b-', label='BFGS', linewidth=2)
plt.plot(iterations, cg, 'm-.', label='Conjugate Gradient', linewidth=2)
plt.axhline(y=3.13, color='k', linestyle=':', label='Optimal D*=3.13')

plt.xlabel('Iteration Number', fontsize=10, fontname='Times New Roman')
plt.ylabel('Objective Function Value D', fontsize=10, fontname='Times New Roman')
plt.title('Convergence Comparison - Case 1', fontsize=11, fontname='Times New Roman')
plt.legend(loc='lower right', fontsize=9)
plt.grid(True, alpha=0.3)
plt.tight_layout()
plt.savefig('Figure2_ConvergencePlot.png', dpi=300, bbox_inches='tight')
plt.show()
```

---

## Python Code to Generate Figure 3 (Method Comparison)

```python
import matplotlib.pyplot as plt
import numpy as np

methods = ['Steepest\nDescent', 'Newton', 'BFGS', 'Conjugate\nGradient']
scores = [3.02, 3.04, 3.02, 3.02]
times = [0.0057, 0.0283, 0.0030, 0.0037]

fig, ax1 = plt.subplots(figsize=(7, 4))

# Bar plot for scores
color = 'tab:blue'
ax1.set_xlabel('Optimization Method', fontsize=10, fontname='Times New Roman')
ax1.set_ylabel('Average Score D', color=color, fontsize=10, fontname='Times New Roman')
bars = ax1.bar(methods, scores, color=color, alpha=0.6, label='Average Score')
ax1.tick_params(axis='y', labelcolor=color)
ax1.set_ylim([2.9, 3.1])

# Add score labels on bars
for bar, score in zip(bars, scores):
    height = bar.get_height()
    ax1.text(bar.get_x() + bar.get_width()/2., height,
             f'{score:.2f}', ha='center', va='bottom', fontsize=9)

# Highlight BFGS
bars[2].set_color('tab:green')
bars[2].set_alpha(0.8)

# Line plot for times
ax2 = ax1.twinx()
color = 'tab:red'
ax2.set_ylabel('Average Time (s)', color=color, fontsize=10, fontname='Times New Roman')
line = ax2.plot(methods, times, color=color, marker='o', linewidth=2, markersize=8, label='Computation Time')
ax2.tick_params(axis='y', labelcolor=color)
ax2.set_ylim([0, 0.035])

# Add time labels
for i, (method, time) in enumerate(zip(methods, times)):
    ax2.text(i, time + 0.002, f'{time:.4f}s', ha='center', fontsize=8, color=color)

fig.tight_layout()
plt.title('Overall Method Performance Comparison', fontsize=11, fontname='Times New Roman', pad=20)
plt.savefig('Figure3_MethodComparison.png', dpi=300, bbox_inches='tight')
plt.show()
```

---

## Summary

**Required Figures:** 3 total
1. Figure 1: Framework flowchart (conceptual)
2. Figure 2: Convergence plot (data visualization)
3. Figure 3: Performance comparison (data visualization)

**Priority:**
- Figures 2 and 3 can be generated from data (Python code provided)
- Figure 1 requires manual creation or can be omitted
- All figures are optional but enhance paper quality

**Note:** IEEE format allows papers without figures if page space is limited. Your comprehensive tables already present all essential numerical results.

