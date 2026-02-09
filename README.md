# Patient-Centric Drug Selection Using Machine Learning

This project utilizes multi-class classification techniques to predict the most appropriate drug for a patient based on their demographic and health profiles (Age, Sex, Blood Pressure, Cholesterol, and Sodium-to-Potassium ratio).

## Project Overview
This project focuses on building a patient-centric drug selection system using Machine Learning techniques. By analyzing patient attributes such as age, gender, blood pressure, cholesterol levels, and sodium-to-potassium ratio, the model predicts the most suitable drug for a patient. The goal is to support data-driven and personalized medical decision-making.

## Objectives
Analyze patient health data for meaningful patterns

Perform data cleaning and exploratory data analysis (EDA)

Engineer relevant features such as age groups

Train and evaluate machine learning models for drug prediction

Build an interpretable and accurate classification system

## Dataset Features
The dataset includes patient-related attributes such as:

Age

Sex

Blood Pressure

Cholesterol

Na_to_K ratio

Drug (Target Variable)

The data is preprocessed to remove duplicates, handle missing values, and improve model performance.

### Technologies Used
Python

Pandas – data manipulation

NumPy – numerical operations

Matplotlib / Seaborn – data visualization

Scikit-learn – machine learning models and evaluation

## Methodology

1. Data Loading & Inspection - Mounted Google Drive and loaded the dataset. Checked for missing values, duplicates, and data types

2. Data Preprocessing - Removed duplicate records, Feature engineering (e.g., age grouping), Encoded categorical variables

3. Exploratory Data Analysis (EDA) - Statistical summaries, Distribution and class balance analysis

4. Model Training - Applied supervised ML classification techniques. Split data into training and testing sets

5. Evaluation - Measured performance using accuracy and other metrics. Compared predictions with actual drug labels

## Results

The trained model successfully predicts the appropriate drug based on patient features, demonstrating the potential of ML in supporting personalized healthcare decisions.
