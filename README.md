Business Problem Summary

A retail chain wants to understand which factors drive monthly sales performance across stores. Leadership is considering strategic decisions about:


Increasing marketing spend
Improving inventory availability
Changing discounting strategy
Reallocating staff
Prioritizing certain store types or regions


This analysis uses regression to identify which factors are most strongly associated with monthly sales.


Dataset Description

File: business_regression_data.xlsx

Structure: 320 observations (store-month combinations)

Key Fields:


Dependent Variable: monthly_sales ($400K-$947K)
Numerical Variables:

marketing_spend, footfall, avg_discount_pct, staff_count
inventory_availability_pct, competitor_distance_km, customer_rating



Categorical Variables:

region (East, North, South, West)
store_type (High Street, Airport, Mall, Residential)



Binary: holiday_flag (0=No, 1=Yes)
Additional: monthly_profit


Data Quality:


6 missing values in competitor_distance_km (filled with median)
8 missing values in customer_rating (filled with median)
All other variables complete



Regression Approach

Simple Linear Regression Models

Three models tested with one independent variable each:


Model 1: Marketing Spend → Sales

Equation: Sales = $560,777 + $2.13 × Marketing_Spend
R² = 0.1672 (16.72% of variance explained)
P-value < 0.001 (Significant)



Model 2: Footfall → Sales ⭐ BEST SIMPLE MODEL

Equation: Sales = $446,411 + $35.68 × Footfall
R² = 0.7363 (73.63% of variance explained)
P-value < 0.001 (Highly Significant)



Model 3: Inventory Availability → Sales

Equation: Sales = $484,814 + $2,217.83 × Inventory_%
R² = 0.0131 (1.31% of variance explained)
P-value = 0.041 (Marginally Significant)





Multiple Regression Model ⭐ BEST OVERALL MODEL

Variables Included:


Numerical: marketing_spend, footfall, inventory_availability_pct, customer_rating, holiday_flag, staff_count
Dummy: region (reference: East), store_type (reference: Airport)


Performance:


R² = 0.8369 (83.69% of variance explained)
Improvement over best simple model: +10.06 percentage points
Interpretation: Model explains 84% of sales variation



Dummy Variable Approach

Categorical Variables Converted:


Region: East (reference), North, South, West
Store Type: Airport (reference), High Street, Mall, Residential


Reference Categories:


Region: East (coefficients show differences vs East)
Store Type: Airport (coefficients show differences vs Airport)


Why? Using reference categories (drop_first=True) avoids multicollinearity and interpretation is clear: coefficients show the effect relative to the baseline category.


Model Comparison Summary

AspectModel 1Model 2Model 3MultipleVariables1 (marketing)1 (footfall)1 (inventory)12R²0.16720.73630.01310.8369Significant?YesYesYesYesPractical Use?WeakStrongVery WeakVery StrongImprovementBaseline+469%-92%+14% vs Model 2

Conclusion: Multiple Regression (Model 4) is best - explains 84% of sales variation.


Final Model Selected

Multiple Regression Model (Model 4)

Reasons:


Highest explanatory power: R² = 0.8369 (explains 84% of sales variation)
Captures complexity: Accounts for multiple factors, not just one
Business relevance: Includes factors leadership cares about
Significant improvement: +14% better than best simple model
Actionable insights: Coefficients show impact of each factor



Business Recommendation

Key Findings:


Footfall is the strongest driver of sales (R² alone = 73.6%)
Multiple factors matter together - adding more variables improves model by 14%
Marketing has significant but modest impact (explains only 16.7% alone)
Inventory availability has weak individual relationship with sales
Regional and store-type differences exist - some locations naturally higher sales


Recommended Actions:


Focus on footfall drivers - this is the primary sales driver
Optimize inventory availability - combined with other factors, it helps
Don't over-spend on marketing alone - effectiveness depends on footfall
Consider store location/type - regression shows regional differences matter
Use the model to predict - estimate sales under different scenarios


Caution: Regression shows association, not necessarily causation. High footfall may result from good location rather than causing sales. Leadership should investigate underlying drivers.


Assumptions and Limitations

Assumptions:


Linear relationships between variables and sales
Independent observations (store-months are roughly independent)
Errors normally distributed
No severe outliers distorting model


Limitations:


Association ≠ Causation: High footfall and high sales may both result from good location
Historical data: Model based on 2025 data - may not reflect future dynamics
Omitted factors: Other variables (e.g., local competition, seasonal trends) not included
Multicollinearity: Some variables may be correlated (not explicitly tested)
Generalization: May not apply to different store formats or markets



Screenshots Included

✓ simple_regression_output.png - Model 2 (Footfall) regression output
✓ multiple_regression_output.png - Multiple regression summary
✓ residuals_preview.png - Predicted values and residual analysis
✓ model_comparison_preview.png - Model comparison table


Analysis Date: June 2026
Data Period: 2025 (monthly observations)
Methodology: Ordinary Least Squares (OLS) Linear Regression
Tools: Python (scikit-learn, scipy), Exce
