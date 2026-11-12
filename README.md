# Advertising A/B Testing Analysis

## Overview

This project analyzes an advertising A/B test to compare conversion performance between users shown an advertisement (`ad`) and a public service announcement (`psa`). The analysis uses Python to explore the data, visualize conversion patterns, and apply statistical tests.

## Objectives

- Compare conversion outcomes between the ad and PSA groups.
- Explore how conversions vary by the day and hour users saw the most ads.
- Use statistical testing to assess whether the observed differences are significant.

## Dataset

The dataset contains **588,101 records** and includes these fields:

- `test group`: `ad` or `psa`
- `converted`: whether the user converted
- `total ads`: number of ads seen
- `most ads day`: day when the user saw the most ads
- `most ads hour`: hour when the user saw the most ads

The notebook removes the index and user ID columns before analysis.

## Analysis

1. Load and inspect the data with pandas.
2. Review summary statistics and category values.
3. Visualize conversion rates by test group, day, and hour.
4. Compare ad and PSA conversion outcomes with an independent-samples t-test.
5. Use one-way ANOVA to examine conversion differences across days and hours.

## Key Findings

- The ad group had a higher conversion rate than the PSA group.
- The notebook reports a statistically significant difference between the groups.
- Conversion rates varied significantly across days of the week (F = 68.39, p ≈ 1.80 × 10⁻⁸⁵) and hours of the day (F = 18.74, p ≈ 7.48 × 10⁻⁷⁷).

## Tools

- Python
- pandas
- Matplotlib
- Seaborn
- SciPy

## Running the Analysis

1. Install the required Python packages:

   ```bash
   pip install pandas matplotlib seaborn scipy
   ```

2. Place `marketing_AB.csv` in the project or data folder.
3. Update the CSV path in the notebook to match its location.
4. Run the notebook cells from top to bottom.

## Note

The reported statistical results are those shown in the project notebook. The exported report does not display the exact t-test statistic or p-value for the ad-versus-PSA comparison.
