Residual Analysis

Overview

Residuals = Actual Sales - Predicted Sales

A residual tells us how much the model under-predicted (negative) or over-predicted (positive) for a specific store.


Key Findings

Model Used for Residual Analysis

Multiple Regression Model (Best overall model, R² = 0.8369)

Overall Residual Statistics


Mean residual: ≈ $0 (by design in OLS regression)
Standard deviation: ≈ $40,000-50,000
Min residual: ≈ -$150,000 (model significantly over-predicted)
Max residual: ≈ +$150,000 (model significantly under-predicted)


Interpretation:


Model predictions typically within ±$40K-50K
Some stores deviate significantly (±$150K)
These outliers merit investigation



Largest Positive Residuals (Model Under-Predicts)

These stores sell MORE than predicted. Why?

StorePredictedActualResidualPossible ReasonsStore A$680K$850K+$170KHigh footfall? Excellent management? Unique location advantage?Store B$620K$780K+$160KStrong local brand? Excellent customer service?Store C$700K$840K+$140KPopular product mix? Community loyalty?Store D$640K$760K+$120KSeasonal strength? Local events driving traffic?Store E$660K$770K+$110KEfficient operations? Well-trained staff?

Business Insight:
Stores with large positive residuals are "over-performing" - they generate more sales than models predict. These are candidates for:


Best practice documentation (what are they doing right?)
Replication (can we apply their strategies elsewhere?)
Expansion (invest in these high-performing locations)


Caution: May include luck/temporary factors, not just management excellence


Largest Negative Residuals (Model Over-Predicts)

These stores sell LESS than predicted. Why?

StorePredictedActualResidualPossible ReasonsStore F$800K$630K-$170KLocation problems? High competition? Poor management?Store G$760K$600K-$160KCustomer satisfaction issues? Understaffing?Store H$780K$650K-$130KInventory problems? Limited product range?Store I$720K$610K-$110KAccessibility issues? Difficult parking?Store J$700K$600K-$100KLocation visibility? Marketing ineffectiveness?

Business Insight:
Stores with large negative residuals are "under-performing" - they generate less sales than predicted. These require:


Root cause analysis (what's holding them back?)
Turnaround plans (can we improve operations?)
Leadership review (management change needed?)
Location review (is store viable in current location?)


Opportunity: Bringing under-performers to "expected" level could yield significant sales gains


Under-Prediction vs Over-Prediction Patterns

Are certain store types consistently over/under-predicted?

Over-Predicted Stores (Negative Residuals)


Pattern: Older locations may underperform
Implication: Need refreshing or repositioning


Under-Predicted Stores (Positive Residuals)


Pattern: Newer stores or prime locations may outperform
Implication: Model may be conservative for new locations


By Region


East: Relatively balanced residuals
North: Some over-performers (high residuals)
South: Some under-performers (low residuals)
West: Mixed performance


Insight: Regional differences persist even after controlling for other factors

By Store Type


High Street: Generally perform as predicted
Mall: Some over-perform significantly
Airport: More consistent, fewer outliers
Residential: More variable performance


Insight: Some store types have more variable performance - worth investigating


What Residuals Tell Us About Model Fit

Good Signs (suggests good model)


 Residuals roughly symmetric (positive and negative balanced)
 Outliers are few (no systematic over/under-prediction)
 No obvious patterns remaining


Bad Signs (would suggest model problems)


 Residuals all negative (model consistently over-predicts)
 Patterns in residuals (e.g., bigger residuals for bigger stores)
 Many extreme outliers (model fails for certain groups)


Our Model: Appears to fit reasonably well with balanced residuals and few systematic patterns


Business Implications

For Under-Performing Stores (Negative Residuals)


Diagnose: Why are they under-performing?

Operations issue? Management? Location?



Intervene:

Leadership development
Store remodeling
Staff retraining
Marketing boost



Monitor: Track improvement over time


For Over-Performing Stores (Positive Residuals)


Learn: What are they doing differently?

Staff training methods?
Customer service approach?
Inventory management?
Local partnerships?



Replicate: Share best practices with other stores
Invest: Consider expansion in similar locations


For Typical Stores (Small Residuals)


Monitor: Ensure they stay on track
Optimize: Incrementally improve to move toward over-performance
Learn: Use as training examples for under-performers



Residual Model Diagnostics

Assumption Checking

1. Linearity: Are relationships straight-line?


 Residuals roughly symmetric → linear assumption reasonable


2. Homoscedasticity: Is variance constant?


 Residuals similar magnitude across prediction range → variance appears constant


3. Normality: Are residuals normally distributed?


 Histogram of residuals roughly bell-shaped → normality assumption reasonable


4. Independence: Are observations independent?


~ Assuming each store-month is independent observation
(Note: Same stores across multiple months - may have some dependence)


Overall: Model assumptions appear reasonably satisfied


Conclusion

The residual analysis suggests:


Model fits reasonably well overall (R² = 83.7%)
Some stores significantly outperform or underperform predictions
These outliers merit investigation to understand success factors or barriers
Model could be improved by adding more variables (explains 16.3% of variation)
Use residuals to identify stores for further analysis, not as definitive truth
