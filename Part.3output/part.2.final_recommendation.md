Final Business Recommendation

Executive Summary

Based on regression analysis of 320 store-months, we recommend using data-driven approaches to optimize sales, with FOOTFALL as the primary focus, while understanding that marketing, inventory, location, and customer experience all play supporting roles.


Which Factors Are Most Strongly Associated with Sales?

Primary Drivers (in order of strength)

1. FOOTFALL  STRONGEST DRIVER


Evidence: R² = 0.7363 (explains 73.6% of sales variation alone)
Impact: Each additional customer → $35.68 sales
P-value: <0.001 (highly significant)
Interpretation: Customer visits are the dominant sales driver
Action: Focus on getting more people into stores (location, accessibility, visibility)


2. MULTIPLE FACTORS COMBINED  BEST OVERALL


Evidence: R² = 0.8369 when combining all factors (83.7% of variation)
Improvement: +10.1% better than footfall alone
Interpretation: Sales driven by combination of factors, not just footfall
Key factors when controlling for footfall:

Marketing spend (modest positive effect)
Inventory availability (supporting role)
Regional location (some regions naturally higher)
Store type (different formats have different sales)
Customer rating (higher satisfaction → higher sales)
Holiday periods (+$25K-30K during holidays)





3. MARKETING SPEND (Moderate Importance)


Evidence: R² = 0.1672 (explains 16.7% alone)
Impact: Each $1 spent → $2.13 sales (simple model) or $1.80 (in multiple model)
P-value: <0.001 (significant)
Interpretation: Marketing works but is NOT the primary lever
Caution: Marketing's effect may depend on footfall (needs customers to sell to)


4. INVENTORY AVAILABILITY (Weak Individual Effect)


Evidence: R² = 0.0131 (explains only 1.3% alone)
Impact: Each 1% inventory increase → $2,217.83 sales
P-value: 0.041 (barely significant)
Interpretation: Weak relationship suggests inventory is rarely the constraint
Possible explanations:

Inventory availability already high across all stores
Customers attracted by location/marketing, not inventory depth
Effect shows up better when combined with other factors (R² improves in multiple model)






Which Variables Should Leadership Focus On?

Priority 1: FOOTFALL DRIVERS (Highest Impact)

Focus: Improve store accessibility and visibility to increase customer visits

Specific actions:


Location optimization: Prioritize high-traffic locations for new/remodeled stores
Accessibility: Easy parking, public transport, convenient hours
Visibility: Better signage, window displays, local marketing
Customer experience: Store layout, cleanliness to encourage repeat visits


Expected impact: High - this is the dominant sales driver


Priority 2: MARKETING + FOOTFALL SYNERGY (Supporting Role)

Focus: Use marketing to drive footfall, not replace it

Specific actions:


Marketing ROI: Market spend effective at ~$1.80-2.13 return per $1 spent

But depends on having customers to sell to (footfall)



Channel optimization: Focus marketing on channels that drive store visits
Promotional strategy: Tie promotions to foot traffic (e.g., "come in Saturday for special")
Regional differences: Some regions respond better to marketing - analyze regional effectiveness


Expected impact: Moderate - works best when combined with footfall strategy


Priority 3: LOCATION & STORE TYPE (Structural Factors)

Focus: Different locations and store types naturally have different sales

Specific actions:


Region strategy:

Analyze why some regions outperform
Replicate successful region strategies in weaker regions



Store type optimization:

Some formats (e.g., Mall) may naturally outperform others (e.g., Airport)
Consider store type when setting sales targets
Invest in high-performing formats





Expected impact: Moderate - built into store model, harder to change


Priority 4: INVENTORY AVAILABILITY (Maintain, Not Priority)

Focus: Keep inventory levels consistent but don't over-invest

Specific actions:


Maintain adequate levels: Current levels appear satisfactory
Don't over-inventory: Marginal gains from higher inventory levels are small
Focus on fast-movers: Ensure popular items always in stock (vs. low-demand items)
Monitor out-of-stocks: Reduce customer frustration, but don't tie up capital excessively


Expected impact: Low - weak individual relationship suggests not a primary constraint


Which Variables Should NOT Be Over-Interpreted?

1. Inventory Availability (Weakest Model)


Why: R² = 0.0131 (explains only 1.3%)
Risk: Tempting to assume inventory drives sales, but evidence is weak
Reality: Other factors (location, footfall) matter more
Action: Maintain adequate inventory but don't prioritize over footfall strategies


2. Individual Marketing ROI


Why: Effect varies with footfall (interaction not directly measured)
Risk: Simple model shows $2.13 return per $1, but real return depends on context
Reality: Marketing works better when targeting high-footfall locations
Action: Don't assume linear marketing effectiveness - it's conditional


3. Regional Differences


Why: Regions may differ due to unmeasured factors (competition, local economy)
Risk: Assuming coefficient = true regional effect
Reality: Regional effect might partially reflect location/demographic differences
Action: Use regional dummies to control for differences, not over-extrapolate



Recommended Business Actions

Immediate Actions (0-3 months)


Footfall Analysis

Identify stores with low footfall
Analyze foot traffic patterns (time of day, day of week, seasonality)
Implement foot-traffic measurement (counters, sensors) if not already done



Marketing Audit

Calculate ROI of current marketing spend by channel
Redirect spend to channels that drive store visits
Reduce spend on channels that don't drive footfall



Location Strategy

Analyze which store locations have highest footfall
Understand what drives high-traffic locations
Plan new stores in similar high-traffic areas





Medium-term Actions (3-6 months)


Store Experience Optimization

Customer rating has positive effect on sales
Improve store experience: cleanliness, layout, checkout speed
Train staff (staff_count variable shows some effect)



Holiday Periods

Model shows $25K-30K sales lift during holidays
Plan ahead: staffing, inventory, marketing for holiday periods
Capitalize on natural seasonal demand



Regional Excellence

Replicate high-performing region practices in other regions
Address regional differences systematically





Long-term Actions (6+ months)


Store Format Optimization

Analyze which store types perform best
Consider expanding best-performing formats
Plan renovations/closures based on performance data






Important Limitations & Risk Factors

1. Regression Shows Association, Not Causation

Example: The model shows high customer ratings are associated with high sales. But does:


A) High satisfaction causes high sales? (good service increases spending)
OR B) High sales cause high ratings? (customers rate us highly because we have good selection due to high sales enabling better inventory)


Risk: Acting on assumption of causation could waste resources

Mitigation: Conduct further analysis (A/B testing, qualitative research) to understand direction

2. Unexplained Variation (16%)

What it means: Even with all these factors, we still can't explain 16% of sales variation

Possible causes:


Local competition (not measured)
Economic conditions (not measured)
Weather/natural events (not measured)
Product mix/category performance (not measured)
Staff quality/manager effectiveness (not measured)


Risk: Model predictions could be off by this amount randomly

Mitigation: Use model for directional guidance, not precise forecasting

3. Data from 2025 Only

Risk: Market conditions, customer behavior, competition may change

Mitigation: Re-run analysis quarterly to detect changes

4. Missing Data Handling

Issue: 14 missing values filled with median


6 missing competitor_distance
8 missing customer_rating


Risk: May bias model if missingness is non-random

Mitigation: Small number of missing values (4.4%) - impact likely minimal


Summary: What Leadership Should Do

DecisionBased OnRecommendationConfidenceIncrease marketing spend?Weak individual effect (R²=0.17)Only if tied to footfall strategyMediumImprove footfall?Strongest driver (R²=0.74)YES - highest priorityHighEnhance customer experience?Rating effect in multiple modelYES - supporting impactMediumMaintain inventory levels?Weak effect (R²=0.013)Current levels adequateLow-MediumFocus on specific regions?Region dummies show differencesAnalyze regional strengthsMediumExpand to new store formats?Format shows impact in multiple modelTest high-performing formats firstMedium
