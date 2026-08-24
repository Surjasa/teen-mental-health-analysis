# Social Media & Teen Mental Health: Statistical Analysis & ML Pipeline

An end-to-end data science pipeline evaluating the relationship between adolescent social media consumption patterns and psychological well-being metrics (anxiety, depression, sleep disruption).

---

## 📌 Project Overview

This research project evaluates how specific social media usage metrics impact teenage mental health outcomes. The primary focus of this workspace is maintaining strict separation between **exploratory statistical inference** and **predictive machine learning workflows**.

* **The Problem:** Clinical datasets regarding mental health frequently exhibit extreme class imbalances (e.g., small percentages of severe outcomes) alongside non-linear demographic confounders.
* **The Solution:** This workspace enforces a strict pipeline architecture—performing hypothesis testing strictly on true observational data while reserving synthetic class balancing (SMOTE) strictly for machine learning training splits to prevent data leakage and $p$-value distortion.

---

## 📁 Repository Layout
---

```text
├── Teen_Mental_Health_Dataset.csv                  # Raw source dataset (Unmodified)
├── data_balancing.ipynb                            # Legacy monolithic notebook (Reference only)
│
├── notebooks/
│   ├── 01_data_inspection_preprocessing.ipynb     # Data cleaning, encoding, train/test split & SMOTE
│   ├── 02_hypothesis_testing_inference.ipynb       # Statistical tests (t-tests, Chi-square, ANOVA, Regression)
│   ├── 03_descriptive_analysis_visualization.ipynb # Summaries, distributions & paper-ready plots
│   └── README.md                                   # Execution guide & notebook-specific notes
│
├── results/                                        # Generated CSVs, statistical tables, and model evaluation metrics
└── reports/                                        # Final figures, visualizations, and summary reports
```
## Core Methodology 
- Raw Data Integrity: Teen_Mental_Health_Dataset.csv remains unedited.
- Inference vs. Synthetic Data: Hypothesis testing (ANOVA, Chi-Square, t-tests) is performed only on the original dataset. SMOTE-generated synthetic rows are strictly excluded from statistical tests to prevent artificial p-value inflation.
- No Data Leakage: Preprocessing, scaling, and SMOTE balancing are applied only to the training split after executing the train-test split.
---
## Execution Order
- 01_data_inspection_preprocessing.ipynb — Inspect raw schema, clean missing values, encode features, and perform train/test split (saving balancing for model training).
- 02_hypothesis_testing_inference.ipynb — Run formal statistical tests (t-tests, ANOVA, Chi-Square, regression) on the original, un-balanced dataset.
- 03_descriptive_analysis_visualization.ipynb — Generate summary statistics, correlation matrices, and distribution plots for report presentation.
---
## Environment Setup
Clone the repository and install dependencies
