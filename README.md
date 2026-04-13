# Anchoring in Movie Ratings

## Objective
This project analyzes whether early movie ratings influence later ratings, testing for potential anchoring effects in user evaluations.

## Data
- Source: MovieLens dataset (~100,000 ratings)
- Variables: movieId, rating, timestamp
- Ratings are ordered over time for each movie

## Methodology
- Defined "early ratings" as the first 20 reviews per movie
- Computed:
  - Early average rating (EarlyAvg)
  - Later average rating (LaterAvg)
- Performed:
  - correlation analysis
  - group comparison (high vs low early ratings)
  - OLS regression

## Results
- Strong positive relationship between early and later ratings
- Group comparison:
  - High early ratings → LaterAvg ≈ 3.88
  - Low early ratings → LaterAvg ≈ 2.87
- Regression results:
  - Coefficient (EarlyAvg): ≈ 0.65
  - R²: ≈ 0.39

## Interpretation
Early ratings strongly predict later ratings, indicating persistence in evaluations. This pattern is consistent with anchoring effects.

## Limitations
The analysis does not establish causality. Results may reflect underlying movie quality rather than behavioral bias.

## Tools
- Python (pandas, matplotlib, statsmodels)
- Jupyter Notebook
