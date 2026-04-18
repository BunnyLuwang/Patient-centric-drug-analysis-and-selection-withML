# Patient-Centric Drug Selection Using Machine Learning

> A multi-class classification system that predicts the most suitable 
> drug for a patient based on their demographic and clinical profile — 
> supporting data-driven, personalized medical decision-making.

---

## Business Problem

Prescribing the right drug to the right patient is a critical challenge 
in clinical care. Mismatched prescriptions lead to treatment failure, 
side effects, and increased healthcare costs. This project builds an 
ML-powered recommendation system that identifies the optimal drug based 
on patient attributes — providing a data-driven aid for clinical teams.

---

## Dataset Features

| Feature | Description |
|---|---|
| Age | Patient age |
| Sex | Gender |
| Blood Pressure | BP level (LOW / NORMAL / HIGH) |
| Cholesterol | Cholesterol level (NORMAL / HIGH) |
| Na_to_K ratio | Sodium-to-Potassium ratio in blood |
| **Drug** | **Target drug type to prescribe** |

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
because its coefficients can be mapped back to patient features — 
allowing clinicians to understand *why* a drug was recommended, not 
just *what* was recommended.

---

## Tech Stack

`Python` `Pandas` `NumPy` `Matplotlib` `Seaborn` `Scikit-learn` 
`imbalanced-learn (SMOTE)` `Jupyter Notebook`

---

## Future Improvements

- Add cross-validation to further validate perfect accuracy claims
- Deploy as a clinical decision-support web app using Streamlit/Gradio
- Extend dataset with more patient records for generalizability
