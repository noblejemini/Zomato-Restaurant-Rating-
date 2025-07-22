# Restaurant Rating Prediction using Machine Learning

This project aims to predict restaurant ratings by analyzing a combination of numerical, categorical, and textual features derived from Zomato data. It explores and compares multiple machine learning models — **Ridge Regression**, **Random Forest**, and **XGBoost** — to determine which best captures the patterns in the data.

---

## Problem Statement

Given various restaurant attributes — such as cost, location, type, and user reviews — build a machine learning model that accurately predicts the restaurant’s **rating** on the Zomato platform.

---

## Approach

### Exploratory Data Analysis
- Studied the distribution of ratings and the correlation with factors like cost, reviews, location, etc.
- Conducted multiple **hypothesis tests** to verify statistically significant features.

### Feature Engineering
- **Missing values** handled with appropriate imputation strategies.
- **Outliers** treated to reduce skewness.
- **Categorical encoding** using one-hot encoding.
- **Text preprocessing** on user reviews: cleaned, tokenized, and vectorized using TF-IDF.
- **Dimensionality Reduction** on sparse vectors using TruncatedSVD to reduce memory usage.
- Combined numeric and text features for model training.

---

##  Models Used & Results

| Model           | MSE   ↓   | R² Score ↑ | Cross-Validated R² ↑ | Notes                         |
|----------------|-----------|------------|------------------------|-------------------------------|
| Ridge Regression | 0.9224  | 0.5794     | 0.5870                 | Baseline linear model         |
| Random Forest   | 0.8784  | 0.5995     | 0.5787                 | Tuned with GridSearchCV       |
| **XGBoost**     | **0.8198** | **0.6262** | **0.6281**             | ✅ Best performing model       |

---

## Final Conclusion

After evaluating multiple models, **XGBoost** proved to be the most accurate and robust in predicting restaurant ratings, achieving the **highest R² score and lowest MSE** on the test set. Feature importance suggests that **cost, type, location, and textual reviews** significantly influence the overall rating.

---


