# Food Contamination Risk Prediction

## Project Overview

This project was developed as part of my Master's thesis and focuses on predicting food contamination risk using machine learning techniques. The goal is to analyze environmental and operational sensor data to identify patterns associated with contamination risk in food supply chains.

The project demonstrates the application of data preprocessing, exploratory data analysis, machine learning modeling, and explainable AI to support early contamination detection and preventive decision-making.

---

## Dataset

The dataset contains simulated environmental and operational monitoring data representing food supply chain conditions.

Key variables include:

* Temperature
* Humidity
* pH Level
* Gas Concentration
* Handling Score
* Seal Integrity
* Cleanliness Index
* Supply Delay
* Contamination Risk (target variable)

The dataset contains **5,000 records** representing simulated supply chain batches. 

---

## Tools & Technologies

* Python
* Pandas
* NumPy
* Scikit-learn
* XGBoost
* Matplotlib
* Seaborn
* SHAP (Explainable AI)
* Jupyter Notebook

---

## Methodology

The project follows a complete machine learning pipeline:

1. Data preprocessing and cleaning
2. Exploratory data analysis (EDA)
3. Handling class imbalance using SMOTE
4. Training machine learning models (Logistic Regression, Random Forest, XGBoost)
5. Model evaluation using ROC-AUC and Precision-Recall metrics
6. Model explainability using SHAP values
7. Risk phenotype identification using K-means clustering

---

## Model Results

The **XGBoost classifier** achieved the best performance.

Key performance metrics:

* **ROC-AUC:** 0.9996
* **PR-AUC:** 0.9997
* **Precision:** 1.000
* **Recall:** 0.850
* **F1 Score:** 0.919
* **Operating Threshold (τ):** 0.988

At the selected threshold, the model achieved **perfect precision with zero false positives**, making it suitable for safety-critical contamination detection scenarios. 

---

## Model Evaluation

### ROC Curve

The ROC curve shows the model’s ability to distinguish contaminated and safe batches.

![ROC Curve](images/roc_curve.png)

---

### Precision-Recall Curve

The Precision-Recall curve demonstrates strong performance even under class imbalance.

![Precision Recall Curve](images/precision_recall_curve.png)

---

### Predicted Probability Distribution

This visualization shows how predicted contamination probabilities separate safe and contaminated batches.

![Probability Distribution](images/probability_distribution.png)

---

## Key Insights

* Environmental conditions such as **humidity, seal integrity, and cleanliness** strongly influence contamination risk.
* The XGBoost model achieved near-perfect discrimination between safe and contaminated batches.
* Explainable AI techniques (SHAP) revealed the most influential risk factors.
* Clustering analysis identified interpretable **risk phenotypes** that can guide preventive supply chain actions.

---

## Project Structure

food-contamination-risk-prediction
│
├── notebook
│   └── food-contamination-risk-analysis.ipynb
│
├── data
│   └── simulated_food_contamination_dataset.csv
│
├── images
│   ├── roc_curve.png
│   ├── precision_recall_curve.png
│   └── probability_distribution.png
│
├── model_results
│
└── README.md

---

## Author

Shama Arzeena
Master's in Data Science
Aspiring Data Analyst
