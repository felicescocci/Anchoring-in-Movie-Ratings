# Anchoring in Movie Ratings

## Objective
This project analyzes whether early movie ratings influence later ratings, testing for potential anchoring effects in user evaluations.

## Data
- Source: MovieLens dataset (~100,000 ratings)
- Variables: movieId, rating, timestamp
- Ratings are ordered over time for each movie

## Methodology
- Sorted ratings chronologically for each movie
- Defined "early ratings" as the first 20 reviews per movie
- Computed:
  - Early average rating (EarlyAvg)
  - Later average rating (LaterAvg)
- Performed:
  - correlation analysis
  - group comparison (high vs low early ratings)
  - OLS regression
- Robustness check:
  - repeated analysis using first 10 ratings as "early"

## Results
- Strong positive relationship between early and later ratings
- Group comparison:
  - High early ratings → LaterAvg ≈ 3.88
  - Low early ratings → LaterAvg ≈ 2.87
- Regression results:
  - Coefficient (EarlyAvg): ≈ 0.65
  - R²: ≈ 0.39
- Robustness:
  - Results remain stable when using first 10 ratings (β ≈ 0.64, R² ≈ 0.40)

## Interpretation
Early ratings strongly predict later ratings, indicating persistence in evaluations. This pattern is consistent with anchoring effects, where initial information may influence subsequent judgments.

## Limitations
The analysis does not establish causality. The observed relationship may reflect underlying movie quality rather than behavioral bias. Identifying causal anchoring effects would require additional controls or experimental data.

## Tools
- Python (pandas, matplotlib, statsmodels)
- Jupyter Notebook
