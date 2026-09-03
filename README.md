# Personal Loans EDA

Exploratory Data Analysis (EDA) on a banking dataset to understand customer 
profiles and behavioral patterns related to personal loan acceptance.

## Problem Statement

Banks need to identify which customer segments are most likely to accept personal 
loan offers. This project performs a thorough EDA to uncover demographic, financial, 
and behavioral patterns that distinguish loan-accepting customers from non-accepting 
ones — laying the groundwork for future predictive modeling.

## Dataset

- **Source:** Kaggle — Personal Loan Dataset
- **Records:** 5,037 bank customers (4,943 after cleaning)
- **Features:**
  - `Age`, `Experience` — Demographics
  - `Income` — Annual income (thousands USD)
  - `Family` — Family size
  - `CCAvg` — Average credit card spending per month
  - `Education` — Education level
  - `Mortgage` — Mortgage value
  - `Securities Account`, `CD Account`, `Online`, `CreditCard` — 
    Banking products held
  - `ZIP Code` — Location
- **Target:** `Personal Loan` — Whether customer accepted loan offer (Yes/No)

## Tech Stack

- Python 3.x
- Pandas, NumPy, SciPy
- Matplotlib, Seaborn
- Google Colab

## Methodology

1. **Data Loading & Inspection** — Identified 13 features, mixed numerical 
   and categorical types
2. **Data Quality** — Detected and removed negative experience values and 
   duplicate records (reduced from 5,037 to 4,943 clean records)
3. **Univariate Analysis** — Distributions of age, income, CCAvg, mortgage 
   using histograms and box plots
4. **Bivariate Analysis** — Relationship between income, education, CCAvg 
   and loan acceptance
5. **Correlation Analysis** — Identified key numerical predictors of loan 
   acceptance
6. **Categorical Analysis** — Analyzed loan acceptance rates across 
   education levels, family size, and banking product ownership
   
## Data Cleaning Summary

- Removed records with implausible age values (over 100 years)
- Removed records with negative Experience and Family values
- Removed duplicate records and reset index
- Total data removed was minimal — dataset integrity preserved

## Key Findings

- **Class imbalance detected** — the majority of customers did not accept a personal 
  loan, creating a significant imbalance in the target variable relevant for future modeling
- **Income and CCAvg** are the strongest numerical predictors of loan acceptance — 
  customers who accepted the loan consistently showed higher values in both variables
- **Family size** shows a positive association with loan acceptance — customers with 
  larger families tended to accept the loan more often
- **Education level** shows a clear positive association — higher education correlates 
  with higher loan acceptance rates
- **CD Account** shows the strongest association among all categorical variables — 
  customers holding a CD Account were notably more likely to accept a personal loan
- **Age and Experience** are highly correlated (Pearson correlation close to 1) — 
  potential multicollinearity to address in future predictive modeling

## What I Learned

- Systematic EDA methodology: inspection → cleaning → univariate → 
  bivariate → correlation
- Identifying class imbalance early and its implications for modeling
- How correlated features (Age/Experience) create multicollinearity risk
- Translating statistical findings into business-relevant insights for 
  banking domain
