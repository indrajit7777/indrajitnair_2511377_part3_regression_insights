# Model Comparison Analysis

## Summary Table

| Aspect | Model 1 | Model 2 | Model 3 | Multiple |
|--------|---------|---------|---------|----------|
| **Name** | Marketing Spend | Footfall | Inventory | Multiple Regression |
| **Variables** | 1 (marketing) | 1 (footfall) | 1 (inventory) | 12 variables |
| **R-squared** | 0.1672 | **0.7363** | 0.0131 | **0.8369** |
| **Interpretation** | 16.7% of variance | 73.6% of variance | 1.3% of variance | 83.7% of variance |
| **P-value (main var)** | <0.001 | <0.001 | 0.041 | <0.001 (overall) |
| **Significant?** | Yes | Yes | Yes | Yes |
| **Business Useful?** | Weak | Strong | Very Weak | Very Strong |

---

## Detailed Model Comparison

### Model 1: Marketing Spend → Sales
**Equation:** Sales = $560,777 + $2.13 × Marketing_Spend  
**R² = 0.1672** (explains 16.72% of sales variation)

**Interpretation:**
- For every $1 increase in marketing spend, sales increase by $2.13
- This is a positive relationship (marketing does help sales)
- However, only 17% of sales variation is explained by marketing alone
- Leaves 83% of variation unexplained

**Business Assessment:** 
- Marketing has impact but is NOT the primary sales driver
- Other factors matter more

---

### Model 2: Footfall → Sales ⭐ BEST SIMPLE MODEL
**Equation:** Sales = $446,411 + $35.68 × Footfall  
**R² = 0.7363** (explains 73.63% of sales variation)

**Interpretation:**
- For every additional customer visiting the store, sales increase by $35.68
- Strong relationship: 73.6% of sales variation explained by footfall alone
- Much more predictive than marketing spend
- Only 26.4% of variation remains unexplained

**Business Assessment:**
- Footfall is the PRIMARY driver of sales
- Most important single factor
- Better to drive more customers into stores than increase marketing budget

---

### Model 3: Inventory Availability → Sales
**Equation:** Sales = $484,814 + $2,217.83 × Inventory_%  
**R² = 0.0131** (explains 1.31% of sales variation)

**Interpretation:**
- For every 1% increase in inventory availability, sales increase by $2,217.83
- VERY WEAK relationship: only 1.3% of variation explained
- Nearly 99% of sales variation is NOT explained by inventory alone
- P-value = 0.041 (statistically significant but practically weak)

**Business Assessment:**
- Inventory availability has minimal individual impact on sales
- This could be because inventory is rarely the constraint (good availability everywhere)
- Or because availability doesn't matter much if no customers in store

---

### Model 4: Multiple Regression ⭐ BEST OVERALL MODEL
**Variables:** marketing_spend, footfall, inventory_availability_pct, customer_rating, holiday_flag, staff_count, region (dummy), store_type (dummy)  
**R² = 0.8369** (explains 83.69% of sales variation)

**Interpretation:**
- Combines multiple factors into single model
- Explains 83.7% of sales variation
- 10.1 percentage points BETTER than best simple model
- Only 16.3% of variation remains unexplained

**Why Better Than Simple Models?**
1. **Footfall effect isolated:** Accounts for footfall specifically, not related factors
2. **Captures interactions:** Marketing + Footfall may have combined effect
3. **Controls for location:** Region and store type dummies account for location differences
4. **Accounts for other factors:** Customer rating, staff, inventory all included
5. **More realistic:** Real world has multiple drivers, not just one

**Business Assessment:**
- Multiple factors drive sales together
- No single "silver bullet" solution
- Need integrated approach considering footfall, marketing, inventory, location, etc.

---

## Key Differences

### Simple vs Multiple Models

**Model 2 (Footfall):**
- Explains 73.6% of variation
- Easy to understand: more customers = more sales
- But ignores other factors

**Model 4 (Multiple):**
- Explains 83.7% of variation
- Harder to interpret but more complete
- Accounts for interaction of factors
- Shows which factors matter WHEN controlling for others

---

## Model Selection Recommendation

### **Use Model 4 (Multiple Regression)**

**Reasons:**
1. **Highest explanatory power:** 83.69% vs 73.63%
2. **Improvement:** +10.06 percentage points over best simple model
3. **Captures reality:** Sales driven by multiple factors, not just one
4. **Actionable:** Shows how each factor contributes when holding others constant
5. **Practical:** Helps predict sales under different scenarios

### **Why Not Model 2?**
- Even though Model 2 is strong (R² = 73.6%), it's incomplete
- Doesn't account for marketing, inventory, location differences
- Leadership needs to understand multiple factors, not just footfall

---

## Limitations

| Limitation | Impact |
|-----------|--------|
| **Model 4 complexity** | Harder to explain (12 variables vs 1-2) |
| **Dummy variables** | Categorical effects may not be reliable |
| **Residual variation** | Still 16.3% of sales unexplained (other factors not measured) |
| **Causation** | Regression shows association, not causation |
| **Data quality** | 14 missing values filled with median |

---

## Conclusion

**Model 4 (Multiple Regression) is recommended** because it:
- Explains the most variation (83.7%)
- Considers multiple business drivers
- Provides actionable insights
- Reflects real-world complexity
- Enables scenario analysis and forecasting

