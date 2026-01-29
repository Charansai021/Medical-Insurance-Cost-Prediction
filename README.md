#  Medical Insurance Cost Prediction

> An end-to-end machine learning project using interpretable linear regression models to predict medical insurance costs, with strong emphasis on EDA, feature engineering, and regularization.

---

## 📌 Project Overview

This project builds a complete **machine learning pipeline** to predict medical insurance costs based on demographic and health-related features.  
Rather than relying on black-box models, the focus is on **interpretability**, **statistical assumptions**, and **EDA-driven modeling decisions**.

The workflow follows an **industry-style approach**, covering:
- Exploratory Data Analysis (EDA)
- Feature engineering
- Baseline and regularized linear models
- Model diagnostics and validation
- Professional GitHub project structure

---

## 📊 Dataset

**Medical Cost Personal Dataset**

### Features
- `age` – Age of the insured individual  
- `sex` – Gender  
- `bmi` – Body Mass Index  
- `children` – Number of dependents  
- `smoker` – Smoking status  
- `region` – Residential region  

### Target
- `charges` – Medical insurance cost (USD)

---

## 🔍 Exploratory Data Analysis (EDA)

Key insights from EDA:
- Insurance charges are **right-skewed**, motivating a log transformation of the target
- Strong linear relationship between **age** and insurance costs
- **Smoking status** is the most influential factor, causing a sharp cost increase
- BMI shows moderate correlation with charges, especially among smokers
- Number of children and region have relatively weaker influence
- No severe multicollinearity among numeric features

EDA techniques used:
- Scatter plots with regression lines
- Box plots grouped by categorical variables
- Correlation heatmap
- Residual analysis

---

## ⚙️ Data Preprocessing

- Log transformation of the target variable (`log1p(charges)`) to reduce skewness
- One-hot encoding of categorical variables
- Feature scaling using `StandardScaler`
- Train-test split for unbiased evaluation

---

## 📈 Modeling Approach

### Baseline Model
- **Linear Regression**
- Assumption checks using residual diagnostics

### Feature Engineering
- Interaction terms to capture non-linear effects:
  - `age × smoker`
  - `bmi × smoker`

### Regularization
- **Ridge Regression (L2)** applied to control model complexity
- Multiple alpha values evaluated to balance bias–variance tradeoff

---

## 🧪 Model Evaluation

Evaluation metric:
- **R² Score**

Key findings:
- Linear regression is appropriate given the observed relationships
- Regularization stabilizes coefficients without harming performance
- Best Ridge model achieves **R² ≈ 0.85**
- Interaction terms significantly improve predictive power

---

## 🏆 Final Model Selection

- **Ridge Regression with interaction features**
- Provides strong generalization and interpretability
- Avoids overfitting while preserving explanatory insights

---

## 📁 Project Structure

