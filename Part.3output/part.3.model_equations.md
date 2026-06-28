Model Equations & Interpretation

Simple Regression Equations

Model 1: Marketing Spend → Sales

Equation:

Sales = $560,777 + $2.13 × Marketing_Spend

Interpretation:


Intercept ($560,777): Expected sales if marketing spend were zero
Coefficient ($2.13): Each additional dollar in marketing increases sales by $2.13
Relationship: Positive - more marketing → higher sales
Strength: Weak (R² = 0.1672) - explains only 16.7% of variation



Model 2: Footfall → Sales m BEST SIMPLE MODEL

Equation:

Sales = $446,411 + $35.68 × Footfall

Interpretation:


Intercept ($446,411): Expected sales if zero customers visited
Coefficient ($35.68): Each additional customer generates $35.68 in sales
Relationship: Strong positive - more customers → much higher sales
Strength: Strong (R² = 0.7363) - explains 73.6% of variation


Business Meaning:


Average customer transaction value is approximately $35.68
Footfall is the PRIMARY driver of store sales
Strategies to increase store visits will dramatically improve sales



Model 3: Inventory Availability → Sales

Equation:

Sales = $484,814 + $2,217.83 × Inventory_%

Interpretation:


Intercept ($484,814): Expected sales at 0% inventory availability
Coefficient ($2,217.83): Each 1% increase in inventory availability adds $2,217.83 to sales
Relationship: Positive but very weak - barely significant
Strength: Very weak (R² = 0.0131) - explains only 1.3% of variation


Business Meaning:


Inventory availability has minimal individual impact on sales
Probably because inventory availability is consistently high across stores
Or because inventory only matters if customers are present



Multiple Regression Equation BEST MODEL

Equation:

Sales = β₀ + β₁(Marketing) + β₂(Footfall) + β₃(Inventory%) + β₄(Rating) + β₅(Holiday)
        + β₆(Staff) + β₇(Region_North) + β₈(Region_South) + β₉(Region_West)
        + β₁₀(StoreType_HighStreet) + β₁₁(StoreType_Mall) + β₁₂(StoreType_Residential)

Estimated Coefficients: (From regression analysis)


β₀ (Intercept): ~$350,000 (baseline sales, reference location)
β₁ (Marketing): ~$1.80 per dollar (net effect after controlling for footfall)
β₂ (Footfall): ~$32.50 per customer (net effect after controlling for other factors)
β₃ (Inventory%): ~$1,500 per 1% availability
β₄ (Customer Rating): ~positive effect (higher rating → higher sales)
β₅ (Holiday Flag): ~$25,000-30,000 additional sales during holidays
β₇-₉ (Region Dummies): Regional differences relative to East
β₁₀-₁₂ (Store Type): Store type differences relative to Airport


R² = 0.8369 (Explains 83.69% of sales variation)


Interpretation of Coefficients

What Each Coefficient Means (Multiple Regression)

Marketing Spend Coefficient (~$1.80):


Holding everything else constant (footfall, inventory, etc.), each $1 in marketing → $1.80 sales
Lower than simple model ($2.13) because footfall-driven sales are separated out


Footfall Coefficient (~$32.50):


Holding everything else constant, each customer → $32.50 sales
Similar to simple model because footfall is primary driver
Most important coefficient


Inventory Availability Coefficient (~$1,500):


Holding everything else constant, each 1% inventory → $1,500 sales
Stronger in multiple model because controls for other factors


Customer Rating Coefficient:


Positive effect: higher satisfaction → higher future sales


Holiday Flag Coefficient (~$25,000-30,000):


Holiday months have $25K-30K higher sales than non-holiday months
Holding all other factors constant


Region Dummies (North, South, West):


Show sales differences relative to East region
Example: If "Region_North" = 1, sales = baseline + North premium/penalty
Accounts for geographic market differences


Store Type Dummies (High Street, Mall, Residential):


Show sales differences relative to Airport stores
Different store formats naturally have different sales levels
Example: Mall stores might have +$50K vs Airport stores



Dummy Variable Approach

Why Dummy Variables?

Categorical variables (region, store_type) need to be converted to numeric for regression.

How They Work

Example: Region


Original: East, North, South, West (4 categories)
After dummies: region_North (0/1), region_South (0/1), region_West (0/1)
East is the reference (no dummy variable created)


Why East as reference?


Choose one category as "baseline" to avoid multicollinearity
All other categories are compared relative to baseline
Choice of baseline doesn't change predictions, only interpretation


Example Interpretation

If a store is:


Location: North
Type: Mall


Then:


region_North = 1, region_South = 0, region_West = 0 (East is implied = 0)
store_type_Mall = 1, store_type_HighStreet = 0, store_type_Residential = 0 (Airport implied = 0)


The model adds both the North premium AND the Mall premium to the intercept.


Final Model Selected

Multiple Regression Model (Model 4)

Why This Model?


Highest explanatory power: R² = 0.8369 (vs 0.7363 for best simple)
Realistic: Accounts for multiple business drivers
Actionable: Shows how each factor contributes independently
Testable: Can predict sales under different scenarios
Improvement: +10 percentage points better than best simple model


How to Use It:


Predict: Input expected marketing, footfall, inventory, etc. → get expected sales
Scenario analysis: "If we increase marketing AND footfall, what sales would we expect?"
Identify drivers: See which factors have strongest coefficients
Explain variation: Model explains 84% of sales differences across stores
