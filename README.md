# Indian Judicial Analysis

## Overview

This project is a judicial analytics research study conducted on the **DAKSH High Court Bail Dataset**, focusing on bail adjudication patterns, judicial efficiency, backlog dynamics, and institutional variation across Indian High Courts.


The objective is to identify measurable structural patterns in Indian High Court bail proceedings using large-scale administrative judicial data.

---

# Dataset

| Component | Description |
|---|---|
| Source | DAKSH High Court Bail Dataset |
| Coverage | Multiple Indian High Courts |
| Time Period | Primarily 2010–2021 |
| Total Cases | ~9.27 lakh bail cases |

### Key Variables

- `NAME_OF_HIGH_COURT`
- `Mapped_Bail`
- `HEARING_COUNT`
- `DISPOSAL_DAYS`
- `PENDING_DAYS`
- `UNDER_ACTS`
- `NATURE_OF_DISPOSAL_OUTCOME`

---

# Phase 1 — EDA & Data Validation

## Objectives

- Validate dataset quality and consistency
- Examine missingness and court-level variation
- Analyze disposal and pendency distributions
- Verify derived judicial metrics

## Key Findings

- Disposal timelines and hearing counts were highly right-skewed.
- Significant institutional variation existed across High Courts.
- Missingness was concentrated in legislation and disposal outcome fields.
- Administrative standardization differed substantially across jurisdictions.

---

# Notebook 1 — Bail Outcome Prediction

## Methods
- Logistic Regression
- Random Forest
- XGBoost
- SHAP Explainability

## Key Findings

| Metric | Value |
|---|---|
| Final modelling dataset | 1,48,040 cases |
| Allowed outcomes | ~68.3% |
| Best ROC-AUC | ~0.70 |

- High Court identity was one of the strongest predictors of bail outcomes.
- Hearing count and bail type materially influenced predictions.
- Moderate predictive performance suggests administrative metadata alone cannot fully explain judicial decisions.

---

# Notebook 2 — Survival Analysis of Bail Disposal

## Methods
- Kaplan–Meier Estimation
- Cox Proportional Hazards Model
- Log-rank Testing

## Key Findings

| Metric | Value |
|---|---|
| Total cases analysed | 9,27,896 |
| Pending cases | 50,914 |
| Log-rank statistic | 25,203.87 |

- Cancellation bail cases showed the slowest disposal patterns.
- Hearing count strongly influenced disposal duration.
- Significant institutional variation existed across High Courts.

---

# Notebook 3 — COVID Interrupted Time Series Analysis

## Methods
- Interrupted Time Series Regression
- Structural Break Analysis

## Key Findings

- COVID-19 caused a major disruption in judicial throughput.
- Disposal rates declined more sharply than filings during lockdown periods.
- Backlog accumulation accelerated post-2020.
- Recovery remained incomplete across several periods.

---

# Notebook 4 — Geographic Justice Gap Analysis

## Methods
- Geographic Aggregation
- Court-Level Comparison
- Delay Distribution Analysis

## Key Findings

- Bail disposal timelines varied significantly across jurisdictions.
- Geographic clustering of delay patterns was observed.
- Certain High Courts consistently exhibited longer disposal durations.

---

# Notebook 5 — Hearing Efficiency & Policy Analysis

## Methods
- Hearing Burden Analysis
- Disposal Efficiency Modelling
- Policy Simulation

## Key Findings

- Hearing count distributions were highly skewed across courts.
- High-hearing cases contributed disproportionately to delay.
- Efficiency simulations suggested that targeted procedural reforms could significantly reduce pendency burden.

---

# Notebook 6 — Legislation-Wise Backlog Analysis

## Methods
- Legislation-Level Backlog Aggregation
- Logistic Regression
- Forecasting & Scenario Analysis

## Key Findings

- IPC-related and special criminal statutes contributed heavily to backlog concentration.
- Certain legislations exhibited systematically longer disposal durations.
- Disposal burden remained highly legislation-dependent during the post-COVID period.

---

# Overall Findings

Across all analyses, several consistent patterns emerged:

- Strong institutional heterogeneity exists across High Courts.
- Procedural complexity is a major driver of judicial delay.
- Geographic inequality affects access to timely bail adjudication.
- COVID-19 significantly disrupted judicial throughput and backlog dynamics.
- Administrative metadata captures meaningful structural patterns but cannot fully explain judicial outcomes.


# Limitations

- Judicial metadata lacks detailed legal reasoning and evidentiary context.
- Administrative practices differ across High Courts.
- Several variables contain substantial missingness and standardization inconsistencies.
- Analyses identify structural patterns rather than causal judicial behaviour.

---

# Author

**Kavish Jain**


