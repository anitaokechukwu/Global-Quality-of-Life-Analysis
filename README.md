# 🌍 Global Quality of Life Analysis using Machine Learning

> **An end-to-end Machine Learning project that analyzes Quality of Life across 236 countries using socioeconomic and environmental indicators. The project applies regression models, clustering, explainable AI (SHAP), and Principal Component Analysis (PCA) to uncover the key drivers of Quality of Life and support data-driven decision-making.**

---

# 📌 Project Overview

Quality of Life is a multidimensional concept influenced by economic strength, healthcare quality, environmental conditions, housing affordability, transportation, and public safety.

This project explores global Quality of Life data to identify the factors that contribute most to living standards and develops predictive machine learning models capable of estimating a country's Quality of Life score.

The project follows a complete data science workflow—from business understanding and exploratory analysis to machine learning, model explainability, dimensionality reduction, and deployment preparation.

---

# 🎯 Business Problem

Governments, policymakers, investors, researchers, and international organizations often rely on multiple socioeconomic indicators when evaluating a country's standard of living. However, determining which factors contribute most to Quality of Life remains challenging.

This project aims to identify the most influential indicators, build predictive models, and group countries with similar living conditions to support evidence-based decision-making.

---

# 🎯 Business Objectives

* Analyze Quality of Life across 236 countries.
* Identify the strongest drivers of Quality of Life.
* Predict Quality of Life using Machine Learning.
* Compare multiple regression models.
* Evaluate model performance using Cross-Validation.
* Explain model predictions using SHAP (Explainable AI).
* Cluster countries with similar socioeconomic characteristics.
* Reduce feature dimensions using PCA for visualization.
* Generate actionable business insights and recommendations.

---

# 📂 Dataset Information

**Dataset Name:** Quality_of_Life.csv

**Records:** 236 Countries and Territories

**Features:** 8 Numerical Indicators + Country Information

### Variables

* Purchasing Power
* Safety
* Health Care
* Climate
* Cost of Living
* Property Price to Income
* Traffic Commute Time
* Pollution
* Quality of Life (Target Variable)

---

# 🛠 Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* SHAP
* Jupyter Notebook

---

# 📊 Project Workflow

```
Business Understanding
        ↓
Data Cleaning
        ↓
Exploratory Data Analysis (EDA)
        ↓
Correlation Analysis
        ↓
Linear Regression
        ↓
Random Forest Regression
        ↓
Hyperparameter Tuning
        ↓
Cross-Validation
        ↓
XGBoost
        ↓
Feature Importance
        ↓
SHAP Explainability
        ↓
K-Means Clustering
        ↓
Principal Component Analysis (PCA)
        ↓
Business Insights
        ↓
Recommendations
```

---

# 📈 Exploratory Data Analysis

The analysis included:

* Data Cleaning
* Missing Value Treatment
* Data Type Conversion
* Descriptive Statistics
* Correlation Analysis
* Distribution Analysis
* Outlier Detection
* Country Ranking
* Heatmap Visualization
* Scatter Plot Analysis

---

# 🤖 Machine Learning Models

Three regression models were developed and evaluated.

| Model             |        R² |       MAE |       RMSE |
| ----------------- | --------: | --------: | ---------: |
| Linear Regression |     0.569 |    17.297 |     22.230 |
| **Random Forest** | **0.816** |     9.798 | **14.513** |
| XGBoost           |     0.791 | **8.887** |     15.461 |

## Best Performing Model

🏆 **Random Forest Regressor**

The Random Forest model explained **81.6%** of the variation in Quality of Life scores while producing the lowest overall prediction error (RMSE).

---

# 🔧 Hyperparameter Tuning

Random Forest hyperparameters were optimized using **GridSearchCV** with 5-fold cross-validation to improve predictive performance and identify the best model configuration.

---

# ✅ Cross-Validation

Model robustness was evaluated using **5-Fold Cross-Validation**.

### Random Forest

* Average R²: **0.629**
* Standard Deviation: **0.197**

### XGBoost

* Average R²: **0.660**
* Standard Deviation: **0.251**

The cross-validation results indicate that both ensemble models generalize reasonably well on unseen data, although performance varies due to the relatively small dataset size.

---

# 🌟 Feature Importance

Both Random Forest and XGBoost consistently identified the same key Quality of Life drivers.

| Rank | Feature                  |
| ---- | ------------------------ |
| 1    | Purchasing Power         |
| 2    | Climate                  |
| 3    | Pollution                |
| 4    | Property Price to Income |
| 5    | Traffic Commute Time     |
| 6    | Health Care              |
| 7    | Safety                   |
| 8    | Cost of Living           |

Purchasing Power emerged as the strongest predictor across all models.

---

# 🔍 Explainable AI (SHAP)

SHAP (SHapley Additive exPlanations) was used to interpret the Random Forest model and explain individual predictions.

SHAP analysis confirmed that:

* Purchasing Power contributes the most to higher Quality of Life predictions.
* Climate has a strong positive influence.
* Pollution negatively impacts predicted Quality of Life.
* Housing affordability also plays an important role.

Unlike traditional feature importance, SHAP provides transparent explanations for each prediction, improving model interpretability.

---

# 🌎 Country Segmentation (K-Means Clustering)

Countries were segmented into four clusters based on socioeconomic and environmental indicators.

| Cluster | Average Quality of Life | Characteristics                                               |
| ------- | ----------------------: | ------------------------------------------------------------- |
| 0       |                  155.04 | High purchasing power, strong healthcare, lower pollution     |
| 1       |                  114.29 | Lower purchasing power, higher pollution                      |
| 2       |                  123.20 | Moderate socioeconomic indicators                             |
| 3       |                  130.42 | Lower purchasing power with moderate environmental conditions |

The clustering analysis revealed distinct Quality of Life profiles that can support benchmarking and policy comparisons.

---

# 📉 Principal Component Analysis (PCA)

Principal Component Analysis (PCA) was applied to reduce eight socioeconomic 
indicators into two principal components for visualization.

### Explained Variance

* Principal Component 1: **32.68%**
* Principal Component 2: **14.64%**

**Total Variance Explained:** **47.33%**

The first two principal components retained nearly half of the total dataset variance,
making them suitable for visualizing country patterns and identifying relationships between socioeconomic indicators.

---

# 💡 Key Business Insights

* Purchasing Power is the strongest predictor of Quality of Life.
* Countries with stronger healthcare systems and safer environments generally achieve higher Quality of Life scores.
* Higher pollution levels and longer commuting times are associated with lower Quality of Life.
* Climate significantly influences overall living standards.
* Housing affordability contributes meaningfully to Quality of Life.
* Random Forest delivered the most accurate overall predictions.
* Countries naturally cluster into four distinct Quality of Life profiles.

---

# 📌 Business Recommendations

Based on the analysis:

* Improve economic opportunities to increase purchasing power.
* Invest in healthcare infrastructure and public services.
* Implement pollution reduction initiatives.
* Promote sustainable urban transportation to reduce commuting times.
* Improve housing affordability through balanced housing policies.
* Use cluster-based benchmarking to compare countries with,
 similar socioeconomic characteristics and guide policy development.

---

# 📁 Project Structure

```
Quality_of_Life_Project/

│── data/
│     └── Quality_of_Life.csv

│── notebooks/
│     └── Quality_of_Life_Analysis.ipynb

│── images/
│     ├── correlation_heatmap.png
│     ├── feature_importance.png
│     ├── shap_summary.png
│     ├── pca_visualization.png
│     ├── clusters.png
│     ├── model_comparison.png

│── models/
│     └── random_forest_model.pkl

│── README.md

│── requirements.txt
```

---

# 🚀 Future Improvements

* Streamlit Web Application
* Model Deployment
* SHAP Waterfall Analysis
* XGBoost Hyperparameter Optimization
* Automated Prediction Pipeline
* Live Dashboard Integration

---

# 📷 Project Visualizations

* Correlation Heatmap
* Distribution Plots
* Feature Importance
* SHAP Summary Plot
* SHAP Waterfall Plot
* PCA Visualization
* K-Means Cluster Visualization
* Model Comparison
* Actual vs Predicted Values

---

# 📬 Contact

## Anita Okechukwu

**Healthcare Professional | Data Analyst | Machine Learning Enthusiast**

* 💼 LinkedIn: *(Add your LinkedIn URL)*
* 💻 GitHub: *(Add your GitHub URL)*
* 🌐 Portfolio: *(Add your Portfolio URL)*
* 📧 Email: *(Add your Email)*

---

## ⭐ Support

If you found this project helpful or interesting, please consider giving this repository a **⭐ Star**.

Your support helps others discover the project and motivates continued development.
