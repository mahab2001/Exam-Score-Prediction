# Student Exam Score Prediction 📊

This project explores **student performance prediction** using the **National Education Longitudinal Study (NELS) dataset**.  
The main goal is to build models that estimate student **exam scores** based on demographics, school-related factors, and prior test scores.

---

## 📂 Project Structure
- `predict_exam_score_from_study_hours.py` → Main script (data preprocessing, visualization, model training & evaluation).
- `NELS.csv` → Dataset used for training and testing.
- `README.md` → Project documentation.

---

## 🚀 Features of the Project
1. **Data Cleaning & Exploration**
   - Checked for missing values
   - Histograms & correlation heatmap
   - Boxplots & pairplots for categorical vs numeric features

2. **Feature Engineering**
   - One-hot encoding for categorical variables (`SEX`, `RACE`, `HSSTAT`, `F4HSTYPE`)
   - Standardization of numerical features

3. **Modeling**
   - Linear Regression (baseline)
   - Polynomial Regression (comparison)
   - Performance evaluated using **MAE, RMSE, R²**

4. **Experimentation**
   - Compared different feature groups (demographics, school-related, test history, all features)
   - Identified that **prior test scores** are the strongest predictors of future performance.

---

## 📊 Results

### 🔹 Baseline Model (Linear Regression)
- MAE: **4.04**  
- RMSE: **5.14**  
- R²: **0.70**

### 🔹 Subject-Level Regression (Math Example)
- MAE: ~3.43  
- RMSE: ~4.48  
- R²: ~0.63  

### 🔹 Polynomial Regression
- Degree 2 & 3 → Performance decreased (overfitting)  
- MAE: ~4.46  
- RMSE: ~5.80  
- R²: ~0.62  

**Takeaway:**  
- Prior academic performance is the strongest predictor of future scores.  
- Baseline Linear Regression provides good performance with **R² = 0.70**, but more advanced models could potentially improve results.
