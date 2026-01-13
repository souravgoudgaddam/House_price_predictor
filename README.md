# 🏠 House Price Prediction Using Machine Learning

## 📌 Project Overview
This project focuses on predicting **house prices** using the **Ames Housing dataset**.  
It applies a complete **machine learning workflow**, including data cleaning, feature engineering, encoding categorical variables, model training, evaluation, and model persistence.

Multiple regression models are trained and compared to identify the best-performing approach for house price prediction.

---

## 🎯 Objectives
- Perform exploratory data analysis (EDA)
- Handle missing values effectively
- Encode categorical features (Ordinal & One-Hot Encoding)
- Reduce feature complexity using cardinality analysis
- Train multiple regression models
- Evaluate models using RMSE and R² score
- Save trained models for future use

---

## 📂 Dataset
**File Name:** `AmesHousing.csv`

### Target Variable
- **SalePrice** – Final sale price of the house

### Dataset Details
- Rows: 2930  
- Columns: 82 (reduced to 192 after encoding)

---

## 🛠️ Libraries Used
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- joblib  

---

## 🔍 Exploratory Data Analysis (EDA)
- Dataset shape, columns, and summary statistics
- Missing value analysis
- Distribution of target variable (`SalePrice`)
- Categorical feature distribution
- Numerical feature relationships using:
  - Pair plots
  - Box plots
  - Scatter plots

---

## 🧹 Data Cleaning & Feature Engineering

### Handling Missing Values
- Dropped columns with **>50% missing values**
- Numerical features imputed using **median**
- Categorical features imputed using **most frequent value**

---

### Encoding Categorical Variables
- **Ordinal Encoding** applied to ordered categorical features:
  - Quality, condition, basement, garage-related features
- **Cardinality Analysis** performed to identify high-cardinality columns
- Dropped high-cardinality feature:
  - `Neighborhood`
- **One-Hot Encoding** applied to low-cardinality nominal features

---

## 🧩 Feature Engineering Summary
- Numerical Imputation
- Ordinal Encoding
- One-Hot Encoding
- Cardinality Reduction
- Final feature set prepared for modeling

---

## 🔀 Train-Test Split
- Features (`X`) and target (`y`) separated
- Train-test split applied
- Test size: 20 samples
- Random state fixed for reproducibility

---

## 🤖 Models Trained

### 1️⃣ Linear Regression
- Baseline regression model

### 2️⃣ Random Forest Regressor
- Ensemble-based model using multiple decision trees

### 3️⃣ Gradient Boosting Regressor
- Boosted ensemble model for improved performance

---

## 📊 Model Evaluation

### Metrics Used
- **RMSE (Root Mean Squared Error)**
- **R² Score**

### Performance Results
| Model | RMSE | R² Score |
|------|------|----------|
| Linear Regression | ~14529 | ~0.943 |
| Random Forest | ~14926 | ~0.940 |
| Gradient Boosting | **~14253** | **~0.946** |

✅ **Gradient Boosting Regressor performed best**

---

## 📈 Model Comparison
- RMSE comparison bar chart
- R² score comparison bar chart
- Visualization confirms Gradient Boosting as the top model

---

## 💾 Model Saving
Trained models were saved using **joblib**:
- Linear Regression model
- Random Forest Regression model
- Gradient Boosting Regression model

These models can be reused for inference without retraining.


pip install pandas numpy matplotlib seaborn scikit-learn joblib
jupyter notebook
