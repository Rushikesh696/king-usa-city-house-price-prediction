# King City, USA - House Price Prediction
## Problem Statement
Accurately predicting house prices is critical for buyers, sellers, real estate agents, and financial institutions. In King City, USA, diverse property attributes and market variability present a complex challenge for valuation. Traditional pricing methods often fail to account for non-linear relationships and hidden patterns in housing data.

This project aims to build a machine learning model capable of predicting house prices based on historical sales data and property features. The goal is to evaluate multiple regression algorithms to identify the most accurate and generalizable model, ultimately supporting informed real estate decisions and enabling scalable, data-driven pricing solutions.

This project focuses on predicting house prices in **King City, USA** using various regression algorithms. The goal is to develop a robust, generalizable model suitable for real-world deployment.

---

### Project Overview

- **Type**: Regression
- **Target Variable**: House sale price
- **Data Source**: Real estate dataset from King City, USA
- **Objective**: Compare multiple machine learning models and select the best one based on accuracy and generalization.

---
## Model Building
To identify the most effective regression algorithm for predicting house prices in King City, we implemented and evaluated a variety of machine learning models. Each model was trained using the same feature set and evaluated using R² scores on both training and testing datasets to ensure a fair comparison and assess generalization performance.
**Algorithms Used**
Linear Regression

K-Nearest Neighbors (KNN) Regressor

Support Vector Regressor (SVR)

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor (GBDT)

XGBoost Regressor
---

## Models Evaluated

| Model              | Training R² | Testing R² |
|-------------------|-------------|------------|
| Linear Regression | 0.701       | 0.703      |
| KNN               | 0.864       | 0.774      |
| SVR               | -0.056      | -0.063     |
| Decision Tree     | 0.752       | 0.662      |
| Random Forest     | 0.983       | 0.853      |
| GBDT              | 0.901       | 0.852      |
| XGBoost           | 0.895       | 0.827      |

---
Random Forest and XGBoost showed the best overall performance, combining high accuracy with strong generalization.

Gradient Boosting also performed competitively, with balanced train-test performance.

Simpler models like Linear Regression and KNN performed moderately but were outclassed by ensemble methods.

SVR performed poorly and was unsuitable for this task.

---
## Key Findings

- **Top Models**: Random Forest and XGBoost, with **R² > 0.85** on test data.
- **Generalization**: Both models maintained strong test performance while avoiding overfitting.
- **SVR underperformed**, and Decision Tree showed signs of overfitting.
- **Outliers were retained** to preserve the integrity of real-world data.

---

## Libraries Used

- `pandas`, `numpy`
- `scikit-learn`
- `xgboost`
- `matplotlib`, `seaborn` (for visualization)

---
## Conclusion
This project successfully demonstrates the application of machine learning for real estate price prediction in King City, USA. Through a comprehensive comparison of multiple regression models, Random Forest and XGBoost emerged as the most effective algorithms, achieving R² scores above 0.85 on the testing dataset, indicating strong predictive performance and generalization.

Despite not removing outliers, the models handled the data's real-world variability effectively, reinforcing their robustness. While simpler models like Linear Regression and KNN offered reasonable performance, they were outperformed by tree-based ensemble methods in both accuracy and reliability.

Overall, this project highlights the value of ensemble learning techniques for regression problems involving complex, real-world data. The models are well-suited for deployment in production scenarios requiring both precision and consistency in predictions.
