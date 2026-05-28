# How to Add Complete Table 2 to Your Word Document

## 🚨 Your Current Table is INCOMPLETE

Looking at your screenshot, you're missing:
- ❌ Bounds (Lᵢ, Uᵢ) - Hours (6 rows)
- ❌ Penalty Coefficient (aᵢ) - 1/hours² (6 rows)

## ✅ RECOMMENDED: Keep as ONE Complete Table

### Why Keep It as One Table?
1. ✅ All parameters for each case are in one place
2. ✅ Easier to reference in text ("see Table 2")
3. ✅ Standard IEEE format for comprehensive parameter tables
4. ✅ Professor's instructions don't require splitting

### Complete Table 2 Structure:

```
TABLE II
PARAMETER VALUES FOR TEST CASES

Parameter | Activity | Case 1: Standard | Case 2: Rainy Day | Case 3: Skill Focus
------------------------------------------------------------------------
Weight (wᵢ) - dimensionless
          | Sleep (t₁)      | 1.0  | 1.0  | 1.0
          | Learning (t₂)   | 0.8  | 0.9  | 1.0
          | Physical Play   | 0.9  | 0.5  | 0.8
          | Creative Play   | 0.7  | 0.8  | 0.6
          | Meals (t₅)      | 0.6  | 0.6  | 0.6
          | Hygiene (t₆)    | 0.5  | 0.5  | 0.5

Ideal Duration (μᵢ) - Hours
          | Sleep (t₁)      | 11.0 | 11.0 | 11.0
          | Learning (t₂)   | 2.0  | 2.5  | 3.0
          | Physical Play   | 2.0  | 1.0  | 1.5
          | Creative Play   | 1.5  | 2.0  | 1.0
          | Meals (t₅)      | 1.5  | 1.5  | 1.5
          | Hygiene (t₆)    | 1.0  | 1.0  | 1.0

Bounds (Lᵢ, Uᵢ) - Hours
          | Sleep (t₁)      | [10.0, 12.0] | [10.0, 12.0] | [10.0, 12.0]
          | Learning (t₂)   | [1.5, 3.0]   | [2.0, 3.5]   | [2.5, 3.5]
          | Physical Play   | [2.0, 4.0]   | [0.5, 1.5]   | [1.0, 2.5]
          | Creative Play   | [1.0, 2.5]   | [1.5, 3.0]   | [0.5, 2.0]
          | Meals (t₅)      | [1.5, 2.5]   | [1.5, 2.5]   | [1.5, 2.5]
          | Hygiene (t₆)    | [0.8, 1.5]   | [0.8, 1.5]   | [0.8, 1.5]

Penalty Coefficient (aᵢ) - 1/hours²
          | Sleep (t₁)      | 0.5  | 0.5  | 0.5
          | Learning (t₂)   | 0.8  | 0.7  | 0.6
          | Physical Play   | 0.4  | 0.6  | 0.5
          | Creative Play   | 0.6  | 0.4  | 0.7
          | Meals (t₅)      | 0.8  | 0.8  | 0.8
          | Hygiene (t₆)    | 0.7  | 0.7  | 0.7
```

## 📝 Steps to Fix Your Current Table in Word:

### Method 1: Add Missing Rows to Existing Table

1. **Position cursor** at the end of the last "Ideal Duration" row (after Hygiene 1.0)
2. **Right-click** → Insert → Insert Rows Below
3. **Add 13 more rows** (1 header + 6 activities for Bounds, 1 header + 6 activities for Penalty)
4. **Copy data** from the structure above

### Method 2: Delete and Recreate Complete Table

1. **Delete your current incomplete table**
2. **Insert → Table** → 5 columns × 27 rows
3. **Import from CSV**: 
   - Use `Table2_Complete.csv` file I just created
   - Or manually type following the structure above

### Method 3: Import from HTML (EASIEST)

1. Open `tables_html_format.html` in your browser
2. **Copy Table 2** (the complete one with all 4 sections)
3. **Paste into Word**
4. **Format** with borders and IEEE style

## 📐 Table Dimensions

**Complete Table 2 should have:**
- **Columns:** 5 (Parameter, Activity, Case 1, Case 2, Case 3)
- **Total Rows:** ~27-28 rows including:
  - 1 header row
  - 7 Weight rows (1 header + 6 activities)
  - 7 Ideal Duration rows (1 header + 6 activities)
  - 7 Bounds rows (1 header + 6 activities)
  - 7 Penalty rows (1 header + 6 activities)

## ⚠️ Alternative: Split into Multiple Tables (NOT RECOMMENDED)

If you absolutely must split, create:
- **Table 2a:** Weight and Ideal Duration parameters
- **Table 2b:** Bounds and Penalty Coefficient parameters

However, this is **NOT recommended** because:
- ❌ Requires two table references in text
- ❌ Separates related information
- ❌ Takes more space
- ❌ Less professional appearance

## ✅ Caption Below Complete Table

After your complete Table 2, add:

> "Table 2 shows the comprehensive parameter set (weights, ideal durations, bounds, and penalty coefficients) for testing the quadratic programming model under different developmental scenarios."

## 🎯 Final Checklist

- [ ] Table has ALL 4 parameter sections (Weight, Ideal, Bounds, Penalty)
- [ ] All sections have 6 activities (Sleep through Hygiene)
- [ ] Units are clearly labeled in parameter headers
- [ ] Numeric values are centered
- [ ] Caption explanation is below table
- [ ] Total rows: ~27-28

Your table should match the one in `ods-v3.md` lines 106-134!



