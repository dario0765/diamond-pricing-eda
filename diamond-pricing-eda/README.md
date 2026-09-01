# Exploratory Data Analysis for Diamond Pricing

## What's in this repo

An exploratory data analysis (EDA) notebook built with Seaborn on the classic `diamonds` dataset (~54,000 diamonds). It covers dataset structure and data cleaning, categorical distributions (cut, color, clarity), a Pearson correlation matrix, and a series of relational plots (scatter, box, and pair plots) examining how carat, cut, color, clarity, depth, and table relate to price.

## Approach

1. Load the dataset and inspect its structure, dtypes, and null values.
2. Clean the data: remove rows with physically impossible measurements (x, y, or z equal to 0) and an extreme measurement outlier that would otherwise distort scale-dependent plots.
3. Explore categorical distributions of cut, color, and clarity.
4. Compute a Pearson correlation matrix across numeric variables, then repeat the carat–price correlation on a log-log scale to test for a power-law relationship.
5. Visualize price against carat, depth, table, clarity, color, and cut using relational and categorical plots, plus a pairplot across carat, depth, table, and price.

## Key insight

Carat (weight) is by far the dominant driver of price, with a linear correlation of 0.92 that increases further on a log-log scale, quantitative evidence that the carat–price relationship follows a power-law shape rather than a straight line. Color shifts the carat level at which prices jump (colorless diamonds reach high prices at lower carat), but this is a secondary effect. Depth and table show essentially no correlation with price (-0.01 and 0.13, respectively): they behave as manufacturing standards that nearly all diamonds meet, not as value differentiators.

## Tools

Python · Pandas · NumPy · Matplotlib · scikit-learn · seaborn 

## Next steps

- Bring in cost/acquisition-price data to turn the business hypotheses (e.g., prioritizing carat over cut, color-based segmentation) into testable pricing or inventory strategies.
- Fit a regression model (e.g., on log(price)) using carat, color, clarity, and cut to quantify each variable's contribution beyond raw correlation.
- Investigate demand/turnover data to validate which segments (currently inferred from supply concentration) actually drive sales.

---
