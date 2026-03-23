# Global Cybercrime Regulation Analysis (2020–2024)

## Overview
This project presents an exploratory data analysis (EDA) of cybercrime regulation trends across 194 countries between 2020 and 2024. The goal is to understand how global cybercrime policies have evolved, identify regional and economic disparities, and generate data-driven research insights into regulatory development.

This analysis goes beyond descriptive statistics by uncovering structural patterns, regional convergence trends, and clustering countries based on regulatory behavior.

---

## Key Objectives
- Analyze global changes in cybercrime regulation over time
- Identify regional and income-based disparities in regulation
- Examine whether lower-performing countries are catching up
- Detect anomalies and outliers in global cybercrime policy
- Group countries using unsupervised learning (K-Means clustering)

---

## Dataset
The dataset contains cybercrime regulation scores for 194 countries, including:
- `score_2020`
- `score_2024`
- `score_change`
- `region`
- `income_level`
- country identifiers

The analysis focuses on understanding **relative improvements, stagnation, and disparities** across regions and income groups.

---

## Methodology

### 1. Data Cleaning & Preparation
- Removed `percent_change` due to instability (NaN/inf values from division issues)
- Verified data types, missing values, and structural consistency
- Prepared dataset for comparative and clustering analysis

---

### 2. Exploratory Data Analysis (EDA)

#### Global Trends
- Global average regulation improved significantly from **~0.67 (2020) to ~0.79 (2024)**
- **57.7% of countries improved**, while only **10.8% worsened**
- Indicates strong global momentum toward improved cybercrime regulation

---

#### Distribution Analysis
- Histogram and KDE plots reveal a clear rightward shift in scores
- Suggests not just improvement, but **overall strengthening of global regulatory systems**

---

#### Regional Analysis
- Regions with lower initial scores (e.g., Africa, Oceania) showed the **highest improvement rates**
- Evidence of a **global "catch-up effect"**
- However, **Middle East and parts of Asia lag behind expectations**, showing slower improvement despite lower baselines

- Europe demonstrates:
  - High consistency
  - Strong convergence toward high regulatory scores

- Some regions exhibit **high internal inequality**, indicating uneven development within the same region

---

#### Country-Level Insights
- **North Korea (0.0 in both years)** identified as a critical anomaly — complete absence of regulation despite global cyber activity
- **Kiribati (+0.766) and Gabon (+0.730)** show the largest improvements, proving rapid regulatory progress is possible
- Several countries act as **"regulatory black holes"** with no measurable progress

---

#### Income-Level Analysis
- Strong **positive correlation** between income level and regulation strength:
  - High-income countries: ~0.96 average (2024)
  - Low-income countries: ~0.50 average (2024)

- However, **lower-income countries are improving faster**
  - Indicates the **gap is closing over time**
  - Suggests global diffusion of regulatory frameworks

---

### 3. Advanced Analysis — Clustering (K-Means)

Countries were clustered based on:
- `score_2020`
- `score_2024`
- `score_change`

Using the **elbow method**, optimal clusters were identified (k ≈ 4).

This revealed distinct groups such as:
- High-performing stable countries
- Rapidly improving nations
- Low-performing stagnant regions
- Mixed-transition countries

This clustering provides a **structural understanding of global regulatory behavior**, beyond simple averages.

---

## Key Insights

- Global cybercrime regulation is **improving significantly**
- A clear **"catch-up" trend** exists among lower-performing regions
- Economic strength still plays a major role, but its influence is **weakening over time**
- Regulatory inequality exists both **between and within regions**
- Some countries remain **structurally disconnected from global regulatory progress**
- Clustering reveals **distinct policy evolution patterns across nations**

---

## Research Questions

This analysis raises several important research directions:

- What factors drive rapid regulatory improvement in developing countries?
- Why do some regions (e.g., Middle East, parts of Asia) lag despite similar starting points?
- How does economic development influence regulatory efficiency vs. adoption?
- Can clustering be used to predict future regulatory trajectories?
- What explains the persistence of "zero-regulation" countries?

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Scikit-learn (K-Means Clustering)
- Jupyter Notebook

---

## Repository Structure
cybercrime-analysis/
│── cybercrime_eda.ipynb # Full analysis notebook
│── data/ # Dataset
│── README.md # Project documentation


---

## Future Work
- Apply predictive modeling to forecast regulatory growth
- Incorporate external variables (GDP, internet usage, governance indices)
- Expand to time-series analysis if multi-year data becomes available
- Explore causal relationships using statistical modeling

---

## Author
Samaya Tiwari  
University of Southern Mississippi  

---

## Note
This project reflects an independent analytical effort to explore real-world policy data and generate research-driven insights. I am actively seeking opportunities to expand this work in a research setting.
