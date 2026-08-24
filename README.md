# Bank Marketing Campaign: Feature Engineering & Preprocessing Pipeline

[![Python 3.8+](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-orange.svg)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/scikit--learn-Preprocessing-yellow.svg)](https://scikit-learn.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

##  Project Overview
This repository contains the first practical assignment for the **Data Mining** course. The project focuses on an end-to-end data preprocessing and feature engineering workflow applied to the **Bank Marketing Dataset** (term deposit subscription prediction).

The primary objective is to transform raw tabular banking data into model-ready features, addressing challenges such as missing value imputation, variable typing, nominal one-hot encoding, and ordinal mapping, followed by an evaluation of preprocessing impact using AutoML.

---

##  Dataset Description
The dataset contains information about customers contacted via a direct marketing campaign promoting long-term bank deposits.

- **Instances:** 41,188 rows
- **Features:** 16 attributes (demographic, socio-economic, and campaign-specific interactions)
- **Target Variable (`y`):** Whether the client subscribed to a term deposit (`yes`/`no`)

### Key Variables & Feature Classification
- **Continuous Features:** `age`, `duration`, `campaign`, `pdays`, `previous`
- **Binary Features:** `default`, `housing`, `loan`, `is_telephone_contact`
- **Nominal Features:** `job`, `marital`, `poutcome`
- **Ordinal Features:** `education`, `month`, `day_of_week`

---

##  Preprocessing Pipeline

1. **Missing Value Handling:**
   - Identified explicit/implicit missing representations (`unknown` treated as `NaN`).
   - Imputed categorical missing attributes using mode imputation.
2. **Feature Categorization:**
   - Structured and mapped attributes into strictly typed containers (`continuous`, `binary`, `nominal`, `ordinal`).
3. **Binary Feature Encoding:**
   - Binarized binary indicators (`yes`/`no` $\rightarrow$ `1`/`0`).
4. **Nominal Feature Encoding:**
   - Applied One-Hot Encoding to non-ordered categorical features using the `prefix_value` naming convention.
5. **Ordinal Feature Mapping:**
   - Applied rank-preserving integer mapping across education levels, days of the week, and calendar months.
6. **Modeling & Impact Evaluation:**
   - Evaluated baseline vs. preprocessed feature sets using an AutoML framework to quantify preprocessing gains.

---


### Prerequisites
Make sure you have Python 3.8+ installed.
```bash
git clone https://github.com/<your-username>/bank-marketing-feature-engineering.git
cd bank-marketing-feature-engineering
pip install -r requirements.txt
```


