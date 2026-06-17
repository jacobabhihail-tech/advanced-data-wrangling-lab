# Customer Churn Data Audit

## Dataset Overview

- Records: 900
- Features: 10
- Target Variable: Churn

---

## Data Quality Findings

- No missing values found.
- No duplicate records found.
- Onboard_date converted to datetime format.
- Dataset is clean and ready for analysis.

---

## Key Insights

### Insight 1: Customer Tenure and Churn

Customers with longer tenure show higher churn rates.

- New Customers: 7.1%
- Medium Customers: 14.0%
- Old Customers: 25.0%

This suggests churn increases as customer tenure increases.

---

### Insight 2: Account Managers

Customers assigned an account manager have a higher observed churn rate.

- No Account Manager: 14.1%
- Account Manager: 19.4%

This relationship requires further investigation and does not imply causation.

---

### Insight 3: Number of Sites

The number of sites is a strong predictor of churn.

Customers with 11+ sites exhibit very high churn rates.

Customers with fewer than 8 sites rarely churn.

This appears to be the strongest churn indicator in the dataset.

---

## Recommendations

1. Investigate customers with high site counts.
2. Monitor long-tenure customers for churn risk.
3. Review account manager assignment strategy.
4. Build a churn prediction model using Num_Sites, Years and Account_Manager.