# Mermaid Flowchart Code

Copy this code and paste it into any of these tools:
- https://mermaid.live/
- https://mermaid.ink/
- GitHub markdown file

```mermaid
flowchart TD
    Start([START])
    Input["INPUT PARAMETERS<br/>Weights (w<sub>i</sub>), Ideal durations (μ<sub>i</sub>)<br/>Penalty coefficients (a<sub>i</sub>), Activity bounds<br/>Pediatric guidelines"]
    Constraints["DEFINE CONSTRAINTS<br/>Σt<sub>i</sub> = 24 hrs (Eq. 2)<br/>L<sub>i</sub> ≤ t<sub>i</sub> ≤ U<sub>i</sub> for all i (Eq. 3)<br/>0.5 ≤ (t₃+t₄)/t₂ ≤ 2.5 (Eq. 4)<br/>t<sub>i</sub> ≥ 0 for all i (Eq. 5)"]
    Objective["QUADRATIC OBJECTIVE<br/>Maximize D = Σw<sub>i</sub>[-a<sub>i</sub>(t<sub>i</sub>-μ<sub>i</sub>)² + c<sub>i</sub>] (Eq. 1)<br/>Subject to constraints"]
    Methods["CLASSICAL OPTIMIZATION<br/>• Steepest Descent<br/>• Newton's Method<br/>• BFGS (Quasi-Newton)<br/>• Conjugate Gradient"]
    Compute["COMPUTE OPTIMAL t*<sub>i</sub><br/>For all activities i = 1,...,6"]
    Decision{"Constraints<br/>Satisfied?"}
    Schedule["OPTIMAL SCHEDULE<br/>t*₁ (Sleep), t*₂ (Learning)<br/>t*₃ (Physical), t*₄ (Creative)<br/>t*₅ (Meals), t*₆ (Hygiene)"]
    Score["DEVELOPMENTAL SCORE<br/>D* = Σw<sub>i</sub>[-a<sub>i</sub>(t*<sub>i</sub>-μ<sub>i</sub>)² + c<sub>i</sub>]"]
    End([END])
    
    Start --> Input
    Input --> Constraints
    Constraints --> Objective
    Objective --> Methods
    Methods --> Compute
    Compute --> Decision
    Decision -->|No| Methods
    Decision -->|Yes| Schedule
    Schedule --> Score
    Score --> End
    
    style Start fill:#4A90E2,stroke:#333,stroke-width:2px,color:#fff
    style Input fill:#FF9966,stroke:#333,stroke-width:2px
    style Constraints fill:#B19CD9,stroke:#333,stroke-width:2px
    style Objective fill:#B19CD9,stroke:#333,stroke-width:2px
    style Methods fill:#B19CD9,stroke:#333,stroke-width:2px
    style Compute fill:#B19CD9,stroke:#333,stroke-width:2px
    style Decision fill:#FFD966,stroke:#333,stroke-width:2px
    style Schedule fill:#90EE90,stroke:#333,stroke-width:2px
    style Score fill:#90EE90,stroke:#333,stroke-width:2px
    style End fill:#4A90E2,stroke:#333,stroke-width:2px,color:#fff
```

## Instructions:

### Option 1: Mermaid Live Editor (Easiest)
1. Go to: https://mermaid.live/
2. Paste the code above
3. Click "Download PNG" or "Download SVG"
4. Save as: `optimization_flowchart.png`

### Option 2: Using Node.js (If installed)
```bash
# Install mermaid-cli
npm install -g @mermaid-js/mermaid-cli

# Generate image
mmdc -i flowchart_mermaid.md -o optimization_flowchart.png -w 1200 -H 1600
```

### Option 3: GitHub Gist
1. Create a GitHub Gist with the mermaid code
2. Take a screenshot of the rendered diagram
3. Or use GitHub's raw view to export

The flowchart will have:
- Blue ovals for Start/End
- Orange for Input
- Purple for all Process steps
- Yellow diamond for Decision
- Green for Output/Results

