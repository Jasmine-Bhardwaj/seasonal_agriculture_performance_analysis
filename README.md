# 🌾 Seasonal Agriculture Performance Analysis

A data analytics project exploring how agricultural performance shifts across India's three growing seasons — Kharif, Rabi, and Zaid — using 4,000 real farm-level records spanning environmental conditions, resource usage, and economic outcomes.

---

## Overview

Farming doesn't perform the same way all year round, but why it changes season to season isn't always obvious from raw numbers alone. This project digs into that question directly, analyzing yield, cost, revenue, and profit across seasons to uncover patterns that are backed by evidence rather than assumption.

Rather than treating this as a generic exploratory exercise, the analysis is built around one central question: how does agricultural performance vary across seasons, and what's actually driving that variation? Every insight in this project ties back to that question, and every conclusion is checked against the data rather than taken at face value.

---

## Problem Statement

Agricultural performance is shaped by seasonal shifts in rainfall, temperature, resource availability, and farming practices, but raw agricultural data alone doesn't clearly explain how or why performance changes from one season to the next. This project investigates those seasonal differences through statistical analysis, identifying meaningful patterns, relationships, and variations within the data, and translating them into practical, evidence-based recommendations.

---

## Dataset

- 4,000 farm-level records across 27 features
- Covers three dimensions: environmental conditions (rainfall, temperature, humidity, soil health), resource inputs (fertilizer, water, irrigation method, seed quality), and economic outcomes (yield, production, cost, revenue, profit)
- File: seasonal_agriculture_performance_dataset.csv

---

## Tools & Technology

Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy (statistical testing), Jupyter Notebook, Google Colab, GitHub

---

## Approach

1. Data cleaning — missing values handled, duplicates removed, consistency checks performed
2. Descriptive statistics and outlier investigation
3. Univariate, bivariate, and multivariate analysis
4. Correlation analysis to identify the strongest relationships in the data
5. Seasonal comparison, validated with one-way ANOVA rather than relying on visual differences alone
6. Four original, independently designed analyses covering ROI by season and crop, regional yield stability, irrigation method effectiveness by season, and risk-adjusted profitability

---

## Key Insights

- Average profit falls from ₹178,914.65 in Kharif to ₹87,689.47 in Rabi, and turns negative at –₹24,804.82 in Zaid — a decline of well over ₹200,000 between the best and worst season.
- Zaid is both the driest and hottest season, with rainfall dropping from 849mm in Kharif to just 305mm, and average temperature climbing to 31°C.
- Water efficiency is the strongest predictor of yield in the dataset (r = 0.915), and it declines in step with profit — from 5.89 in Kharif to 4.41 in Zaid.
- No single irrigation method wins across every season — Rainfed leads in Kharif (8.85 vs Sprinkler's 4.62) but nearly loses that edge by Zaid (5.48 vs 4.86).
- State-level yield differences are not statistically significant (ANOVA p = 0.653) despite a visible range of 4.63 to 6.12 tonnes/ha — season matters far more than geography here.
- Sugarcane stays profitable in every season (187% ROI in Kharif, still 104% in Zaid), while Rice, Wheat, and Maize post losses across all three.
- Zaid isn't just less profitable — it's a riskier bet too, with a negative risk-adjusted return (–₹1,235 per unit of disease/pest risk) compared to Kharif's ₹3,585.
- Profit carries the highest outlier rate in the dataset at 10.10% of farms, versus effectively none in environmental variables like rainfall or soil pH.
- A one-way ANOVA confirms profit differs significantly across seasons (p < 0.00001), while yield does not (p = 0.214) — meaning the profit decline isn't a yield story at all.

Full insights, supporting evidence, and honest limitations for each are documented in the notebook.

---

## Recommendations

- Weight planning, credit support, and resource allocation toward Kharif, which delivers both the highest profit (₹178,915) and the best risk-adjusted return, while treating Zaid — which runs at a net loss of –₹24,805 — as a priority for intervention.
- Prioritize water efficiency improvements in Rabi and Zaid, where efficiency drops to as low as 4.41, given its strong link to yield (r = 0.915) and its decline in step with profit.
- Reassess irrigation method choice season by season rather than defaulting to one method year-round, since Rainfed's near 2x efficiency advantage in Kharif nearly disappears by Zaid.
- Base planning guidance on crop-season combinations rather than geography, since regional yield differences aren't statistically significant (p = 0.653) while crop choice clearly is — Sugarcane holds 104–187% ROI across every season.
- Identify and support the specific farms driving the biggest losses rather than relying on seasonal averages alone, given that profit carries a 10.10% outlier rate compared to near-zero in environmental variables.

---

## Limitations

Relationships identified here are correlational, not proof of causation. The lack of a statistically significant regional effect doesn't rule one out entirely, as it may simply be masked by high variability within each state. Outliers in profit and production were deliberately kept rather than removed, since they reflect genuine extreme outcomes rather than data errors, though this means some seasonal averages may be slightly influenced by them. The analysis also relies entirely on the dataset as given, with no independent way to verify how the underlying data was collected.

---

## Future Scope

- Incorporating multi-year data to check whether these seasonal patterns hold consistently over time or shift with year-to-year climate variation
- Connecting real-time weather and market-price feeds to turn this into a live, continuously updating dashboard
- Exploring predictive modeling in a future phase, once the project scope moves beyond pure analytics
- Expanding the dataset to cover more regions and crop types to test how well these findings generalize

---

## End Users

Farmers and agricultural planners making season-aware decisions, agricultural extension officers and policy advisors shaping regional support programs, agri-business and supply chain teams planning around seasonal output, and researchers or students studying agricultural data patterns.

---

## Repository Structure

01_data/
├── 01_raw/
│   └── seasonal_agriculture_performance_dataset.csv
└── 02_processed/
    └── cleaned_seasonal_agriculture_performance_dataset.csv

02_notebook/
└── Seasonal_Agriculture_Performance_Data_Analytics.ipynb

03_visualizations/
├── 01_seasonal_comparison.png
├── 02_anova_statistical_test.png
├── 03_correlation_heatmap.png
├── 04_irrigation_season_heatmap.png
└── 05_roi_by_season_crop.png

---

## How to Run

1. Clone this repository
2. Open notebook/Seasonal_Agriculture_Performance_Data_Analytics.ipynb in Jupyter or Google Colab
3. Upload data/raw/seasonal_agriculture_performance_dataset.csv into your working directory (or Colab session)
4. Run all cells from top to bottom

---

## Author

Jasmine Bhardwaj
2026
