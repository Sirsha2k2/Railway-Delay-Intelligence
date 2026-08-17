# Railway-Delay-Intelligence
# Railway Delay Intelligence

A data-driven analytics project for identifying, quantifying, and visualizing railway delay patterns using **SQL, Python, statistical hypothesis testing, feature engineering, and Power BI**.

## Overview

This project analyzes **312K+ railway journeys** to identify factors associated with delays and uncover high-risk operational segments. The analysis combines large-scale SQL querying with Python-based statistical testing and interactive Power BI dashboards.

The study focuses on the relationship between railway delays and factors such as **train type, congestion, weather conditions, journey duration, and departure patterns**.

## Objectives

- Analyze large-scale railway journey data using SQL.
- Identify key factors associated with railway delays.
- Evaluate relationships between congestion, journey characteristics, and delays.
- Statistically compare journey-time distributions across different segments.
- Develop risk segments based on train type, congestion, and weather.
- Visualize railway reliability patterns through Power BI dashboards.

## Tech Stack

- **Python:** Pandas, NumPy, SciPy
- **SQL:** CTEs, aggregations, window functions
- **Statistics:** Spearman Correlation, Mann–Whitney U Test, Kruskal–Wallis Test
- **Visualization:** Power BI

## Methodology

### 1. Data Cleaning & Preprocessing

- Removed duplicate records and handled missing values.
- Standardized categorical and numerical variables.
- Converted date/time fields into analytical features.
- Created delay indicators and journey-time metrics.

### 2. Feature Engineering

Key engineered features include:

- `is_delayed`
- `severe_delay`
- `journey_time_difference`
- `delay_ratio`
- `peak_hour`
- `weekend`
- `congestion_level`
- `delay_risk`

Delay risk was categorized into:

- On-Time
- Minor Delay
- Moderate Delay
- Severe Delay

### 3. SQL Analysis

SQL was used to perform large-scale exploratory analysis using:

- Common Table Expressions (CTEs)
- Aggregations
- Conditional calculations
- Window functions
- Train-level reliability ranking
- Delay-rate analysis
- Congestion and weather segmentation

### 4. Statistical Analysis

#### Spearman Rank Correlation

Used to evaluate monotonic relationships between railway delays and numerical variables such as congestion, distance, and journey duration.

#### Mann–Whitney U Test

Used to compare journey-time distributions between delayed and on-time journeys.

#### Kruskal–Wallis Test

Used to evaluate whether journey-time distributions differed significantly across train types and weather conditions.

Statistical significance was evaluated at:

**α = 0.05**

### 5. Risk Segmentation

Created **6+ risk segments** by combining:

- Train type
- Congestion level
- Weather condition

Each segment was evaluated using metrics such as:

- Average delay
- Median delay
- Delay rate
- Severe-delay rate
- Average journey time

## Key Findings

- Analyzed **312K+ railway journeys** using SQL and Python.
- Identified segments exhibiting **18.6% higher delay exposure** under selected operational conditions.
- Applied non-parametric statistical tests to identify significant differences in journey-time distributions.
- Identified **6+ high-risk segments** across train type, congestion, and weather.
- Developed interactive Power BI dashboards to compare railway reliability across operational segments.

> Numerical findings are generated from the underlying dataset and analysis pipeline.

## Project Structure

```text
Railway-Delay-Intelligence/
│
├── data/
│   └── railway_journeys.csv
│
├── notebooks/
│   └── railway_delay_analysis.ipynb
│
├── sql/
│   └── railway_delay_analysis.sql
│
├── outputs/
│   ├── railway_cleaned_data.csv
│   ├── railway_powerbi_dataset.csv
│   ├── spearman_results.csv
│   └── delay_risk_summary.csv
│
├── dashboard/
│   └── railway_delay_dashboard.pbix
│
├── railway_delay_analysis.py
├── requirements.txt
└── README.md
