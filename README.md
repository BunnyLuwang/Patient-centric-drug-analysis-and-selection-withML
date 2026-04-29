# Patient-Centric Drug Selection Using Machine Learning

> A multi-class classification system that predicts the most suitable
> drug for a patient based on their demographic and clinical profile -
> supporting data-driven, personalized medical decision-making.

---

## Problem

Prescribing the right drug to the right patient is a critical challenge
in clinical care. Mismatched prescriptions lead to treatment failure,
side effects, and increased healthcare costs. This project builds an
ML-powered recommendation system that identifies the optimal drug based
on patient attributes - providing a data-driven aid for clinical teams.

---

## Dataset Features

| Feature | Description |
|---|---|
| Age | Patient age |
| Sex | Gender |
| Blood Pressure | BP level (LOW / NORMAL / HIGH) |
| Cholesterol | Cholesterol level (NORMAL / HIGH) |
| Na_to_K ratio | Sodium-to-Potassium ratio in blood |
| **Drug** | **Target — drug type to prescribe (A/B/C/X/Y)** |

---

## Power BI Dashboard
<img width="1321" height="737" alt="Screenshot 2026-04-27 204725" src="https://github.com/user-attachments/assets/8fa2b228-7136-42a0-9007-44d790d8c1fe" />


### KPI Summary

| Metric | Value |
|---|---|
| Total Patients Analyzed | 235 |
| Most Prescribed Drug | drugY (108 patients, 45%) |
| Average Na-K Ratio | 16.15 |
| Largest Patient Group | High BP (93 patients, 39.6%) |

### Key Insights

- **drugY is the most prescribed drug** across all age groups and both
  genders, accounting for 45% of all prescriptions (108 out of 235
  patients)
- **drugY patients have a dramatically higher average Na-K ratio (22)**
  compared to all other drugs which cluster between 10–12 - confirming
  drugY targets a clinically distinct patient profile requiring higher
  sodium-to-potassium management
- **High BP patients form the largest segment** (93 patients, 39.6%),
  with a near-equal split between HIGH and NORMAL cholesterol levels
  (42 vs 51) - indicating cholesterol alone does not determine BP severity
- **Gender has minimal impact on drug prescription** - drugY is the
  top prescribed drug for both females (57) and males (51), suggesting
  clinical indicators (BP, Na-K ratio) are stronger prescribing factors
  than demographics
- **drugY prescription increases with age** - dominant across 30–40,
  40–50, and 60+ age bins, suggesting older patients disproportionately
  require Na-K ratio management

### Recommendations

- **Prioritize Na-K ratio monitoring for drugY patients** - their
  significantly higher ratio (22 vs ~11 average) indicates a distinct
  physiological profile requiring closer clinical tracking
- **Accurate drug-type assignment for High BP patients has the highest
  population impact** - as the largest segment (39.6%), errors in drug
  selection for this group affect the most patients
- **Focus prescription accuracy on drugY and drugX** - together they
  account for ~70% of all prescriptions; improving model confidence for
  these two classes delivers the greatest clinical benefit

---

## Methodology

**1. Data Cleaning & Inspection**
- Checked for missing values, duplicates, and data type issues
- Removed duplicate records

**2. Feature Engineering**
- Created age group bins for improved model interpretability
- Encoded categorical variables (Sex, BP, Cholesterol)

**3. Exploratory Data Analysis**
- Statistical summaries and distribution analysis
- Class balance analysis before and after SMOTE

**4. Class Imbalance Handling**
- Applied **SMOTE** (Synthetic Minority Oversampling Technique)
  to balance drug class distribution before training

**5. Model Training & Evaluation**
- Trained 4 supervised ML classifiers
- Evaluated using Accuracy, Precision, Recall, and F1-Score

---

## Model Comparison Results

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---|---|---|---|
| **Logistic Regression** | **100%** | **1.00** | **1.00** | **1.00** |
| Gaussian Naïve Bayes | 100% | 1.00 | 1.00 | 1.00 |
| Decision Tree | 95% | 0.96 | 0.95 | 0.95 |
| Random Forest | 93% | 0.95 | 0.93 | 0.94 |

> **Note:** Perfect scores for Logistic Regression and Gaussian NB are
> consistent with this dataset's well-defined decision boundaries
> post-SMOTE balancing and feature engineering. Logistic Regression
> was selected as the final model for its interpretability advantage
> in a clinical context.

---

## Business Insight

In a clinical setting, interpretability matters as much as accuracy.
Logistic Regression was chosen over Gaussian NB (despite equal scores)
because its coefficients can be mapped back to patient features -
allowing clinicians to understand *why* a drug was recommended, not
just *what* was recommended.

The Power BI dashboard further validates this - Na-K ratio emerges as
the single strongest differentiator between drugY and all other drugs,
which aligns with Logistic Regression's feature coefficient analysis.

---

## Tech Stack

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn`
`imbalanced-learn (SMOTE)` `Power BI` `Jupyter Notebook`

---

## Future Improvements

- Add cross-validation to further validate perfect accuracy claims
- Deploy as a clinical decision-support web app using Streamlit
- Extend dataset with more patient records for generalizability
- Add patient allergy data to further refine drug recommendations
