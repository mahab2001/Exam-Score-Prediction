# Student Exam Score Prediction 📊

This project explores **student performance prediction** using the **National Education Longitudinal Study (NELS) dataset**.  
The main goal is to build models that estimate student **exam scores** based on demographics, school-related factors, and prior test scores.

---

## 📂 Project Structure
- `predict_exam_score_from_study_hours.py` → Main script (data preprocessing, visualization, model training & evaluation).
- `NELS.csv` → Dataset used for training and testing.
- `README.md` → Project documentation.

---

Data Exploration & Visualization:

Checked missing values, distributions, and correlations.

Visualized feature relationships with histograms, heatmaps, and pairplots.

Feature Engineering:

One-hot encoding of categorical variables (SEX, RACE, HSSTAT, F4HSTYPE).

Standardization of numerical features.

Modeling Approaches:

Baseline Linear Regression (All Features)

All available features except the target were used.

Performance:

MAE: 2.92

RMSE: 3.76

R²: 0.79

Correlation-Filtered Regression

Selected only features with correlation > 0.3 with target (F22XMSTD).

Performance:

MAE: 2.91

RMSE: 3.76

R²: 0.79

Tree-Based Feature Selection + Linear Regression

Used RandomForestRegressor to rank feature importance.

Selected top 15 features.

Trained a linear regression model on this reduced feature set.

Performance:

MAE: 2.91

RMSE: 3.76

R²: 0.79

Polynomial Regression was also tested but did not improve performance compared to linear regression.

⚖️ Key Findings

Prior test scores (Math, Reading, Science across different years) were the strongest predictors of future Math scores.

Adding all features did not significantly improve performance compared to a smaller, correlation-based feature set.

Tree-based feature selection highlighted the same set of predictors, confirming their importance.
