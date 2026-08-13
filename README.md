# Housing Prices: A Statistical Analysis in Excel
A team project that analyzes housing prices across six assignments ranging from dataset selection, descriptive statistics, probability, hypothesis testing, and multiple linear regression

## Dataset
- **source**: Housing Prices Dataset, Kaggle
- **Observations**: 545 homes
- **Main variable of interest**: price

## Assignment Summaries
**Assignment 2** *Dataset Selection*

Selected and loaded the Housing Prices dataset; identified price as the primary variable of interest

**Assignment 3** *Descriptive Statistics*

Calculated mean, mode, standard deviation, and other summary statistics for for each variable, and built basic visualizations. Found that air conditioning - not bed rooms or stories - was one of the strongest visible price signals

**Assignment 4** *Probability*

Explored normal vs empirical probability distributions for key variables. Due to heavy right skew in data, used empirical distributions to answer probability questions

**Assignment 5** *Hypothesis Testing*

Ran two one-sample t-tests at α = 0.05
- H0: μ ≤ 5,000 sq ft
- H0: μ ≥ $4.5M
Also computed a 95% confidence interval for mean home price

**Assignment 6** *Regression*

Built a multiple linear regression model to predict price:
- Model 1 - All 12 predictors
- Model 2 - Removed statistically insignificant predictors

## Key Findings
- Bathrooms and stores have an outsized effect on price relative to raw square footage (each bathroom adds ~$1.02M, each store ~$487K vs ~4247 per additional square foot)
- Hot water heating, though present in only ~5% of homes, has the single largest price impact of any amenity (+$860K)
- Furnishing status matters, unfurnished homes sell for ~$374K less than semi-furnished homes

## Business Takeaways
- Prioritize adding bathrooms or full stories over expanding floor space when investing in renovation or new construction
- Furnish or semi-furnish a home before selling as unfurnished homes bring a lower price
- Do not rely on home size alone for pricing strategy. Our area result was too close to the test threshold to be a stand along signal
- $4.5M is a reasonable pricing/loan-qualification floor for this market, with $4.6M-$4.9M as the estimated true average

## Model Limitations 
- R-squared (68%) is acceptable for this exercise but would be low for a production pricing model. Additional variables such as lot shape, school district, and seasonality, could improve fit
- Linear regression assumes linear relationships. Real housing markets often show diminishing returns or interaction effects
- The intercept is not statistically significant, so the model's baseline anchor point should not be over-interpreted
