# Patient-Centric Drug Selection with Machine Learning

This project utilizes multi-class classification techniques to predict the most appropriate drug for a patient based on their demographic and health profiles (Age, Sex, Blood Pressure, Cholesterol, and Sodium-to-Potassium ratio).

## Project Overview
Choosing the right medication is critical for patient outcomes. This project automates the selection process among five different drug types by analyzing patient health indicators. It demonstrates a complete end-to-end data science workflow:

**Data Cleaning & Preprocessing:** Handling categorical variables and feature scaling.

**Exploratory Data Analysis (EDA):** Visualizing distributions and relationships between health metrics.

**Model Building:** Implementing Decision Tree and Random Forest classifiers.

**Evaluation:** Assessing performance using Confusion Matrices and Accuracy scores.

## Dataset Features
The model is trained on patient records with the following features:

**Age:** Age of the patient.

**Sex:** Gender of the patient (F/M).

**BP:** Blood Pressure levels (Low, Normal, High).

**Cholesterol:** Cholesterol levels (Normal, High).

**Na_to_K:** Sodium-to-potassium ratio in the blood.

**Drug (Target):** The drug prescribed (DrugY, drugX, drugA, drugC, drugB)

### Technologies Used
Python (Google Colab environment)

Pandas & NumPy: For data manipulation and analysis.

Scikit-Learn: For machine learning modeling and preprocessing.

Matplotlib & Seaborn: For data visualization.

The Decision Tree Classifier achieved high accuracy in distinguishing between the five drug classes.

Identified Na_to_K ratio and Age as significant predictors in the drug selection logic.
