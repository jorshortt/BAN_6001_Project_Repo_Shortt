# Decision Log
## Assignment 2: Dataset (2026-07-19)
- Dataset: Housing Prices from Kaggle (https://www.kaggle.com/datasets/yasserh/housing-prices-dataset/data)
- Main variable of interest: Prices because this was a continuous variable with the most real world application. All other variables were clearly there to help point to price.
- Key decision: We chose a housing data set as our team has a strong background in economics. We felt that this data would be reflective of our interests and skill sets.
## Assignment 3: Descriptive Stats (2026-07-26)
- Descriptive statistics such as mean, mode, standard deviation, and others calculated.
- Basic data visualizations for each variable created
- Most surprising pattern: Air conditioning, not bedrooms or stories, is one of the strongest price signals
## Assignment 4: Probability (2026-07-26)
- Normal vs. empirical, and why: empirical
- Our team chose due to the heavy right skew of the data in our primary areas of interest. Assuming a normal distribution would not have allowed us to properly understand probability.
## Assignment 5: Inference (2026-08-07)
- We ran two one-sample t-tests at alpha = 0.05.
-   (1) Right-tailed test on area, H0: μ ≤ 5,000 sq ft vs. Ha: μ > 5,000 sq ft — t = 1.62, p = 0.053. Since p is just above alpha, we failed to reject H0; borderline, but not enough evidence the average home is over 5,000 sq ft.
-   (2) Left-tailed test on price, H0: μ ≥ $4.5M vs. Ha: μ < $4.5M — t = 3.33, p ≈ 1.00. We failed to reject H0; no evidence average price is below $4.5M. A 95% CI put the true mean price between $4.6M and $4.9M.
## Assignment 6: Regression (2026-08-12)
- First predictor removed and why: Bedrooms, removed after Model 1 (all 12 predictors) showed it had the highest p-value (0.114) — the only predictor above alpha = 0.05. Removing it barely moved R² (68.0% → 67.8%), confirming it added negligible explanatory value once area and bathrooms were already in the model.
- Multicollinearity handling: Built a correlation matrix for the five continuous/count predictors (area, bedrooms, bathrooms, stories, parking). No pair reached the 0.7 threshold for concern — the highest was bedrooms/stories at r ≈ 0.41 (moderate, not problematic). Since nothing crossed the threshold, no variables were dropped for multicollinearity; bedrooms was dropped separately, for insignificance, not collinearity. Binary/dummy predictors (mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishing dummies) were excluded from this matrix since they aren't continuous.
