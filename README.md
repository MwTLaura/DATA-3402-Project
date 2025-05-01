![UTA-DataScience-Logo](https://github.com/user-attachments/assets/fec1b411-bda5-437a-9eb8-08a018eb84ae)

# 📚 Customer Churn Prediction - Playground Series S4E1

## 📌 One Sentence Summary

This notebook predicts customer churn using data from the [Kaggle Playground Series - Season 4, Episode 1](https://www.kaggle.com/competitions/playground-series-s4e1).

---

## 📋 Overview

The task is to predict whether a customer will leave a bank based on their personal and account details.  
We approach this as a binary classification problem using Logistic Regression, Random Forest, and Gradient Boosting models.  
The best model (Gradient Boosting) achieved a validation AUC of ~87%.

---

## 📂 Data

- CSV files from Kaggle (train.csv and test.csv)
- 165,034 training samples
- Features include credit score, age, tenure, balance, etc.
- Target column: `Exited` (0 = stayed, 1 = churned)

---

## 🛠️ Preprocessing

- Dropped: `id`, `CustomerId`, `Surname`
- Scaled numerical features using StandardScaler
- One-hot encoded `Geography` and `Gender`
- No missing or duplicate values

---

## 📊 Data Visualization

- Histograms for all numerical and categorical features
- Compared churn vs non-churn distributions
- Key predictive features: `Age`, `IsActiveMember`, `NumOfProducts`, `Geography`

---

## 🎯 Problem Formulation

- **Input**: Cleaned customer features
- **Output**: Churn flag (Exited)
- **Models**: Logistic Regression, Random Forest, Gradient Boosting
- **Metric**: Accuracy Score

---

## 🏋️ Training

- Python with scikit-learn
- Training on standard laptop (CPU)
- No hyperparameter tuning
- Gradient Boosting performed best overall

---

## 📈 Performance Comparison

| Model               | Validation AUC |
|---------------------|----------------|
| Logistic Regression | ~0.84          |
| Random Forest       | ~0.86          |
| Gradient Boosting   | ~0.87          |



---

## 📋 Conclusions

- Gradient Boosting was most effective
- Simpler models like Logistic Regression performed reasonably well
- Data quality and feature engineering were more important than algorithm choice

---

## 🚀 Future Work

- Try XGBoost, LightGBM, or CatBoost
- Apply hyperparameter tuning (GridSearchCV)
- Perform deeper feature selection and engineering.

---

## 🔁 How to Reproduce Results

1. Install required packages: `pip install pandas scikit-learn matplotlib numpy`  
2. Download `train.csv` and `test.csv` from [Kaggle Playground S4E1](https://www.kaggle.com/competitions/playground-series-s4e1)  
3. Open the notebook `churn_prediction.ipynb`  
4. Run all cells from top to bottom  
5. The notebook saves `cleaned_train.csv` and generates `submission.csv` for Kaggle  

---

## 🗂️ File Structure

| File              | Description                                           |
|-------------------|-------------------------------------------------------|
| `churn_prediction.ipynb` | Main notebook with all steps: preprocessing, training, evaluation, and submission |
| `cleaned_train.csv`      | Scaled and encoded training data used for modeling |
| `submission.csv`         | Final submission file for Kaggle leaderboard     |

---

## 📚 Citations

- Kaggle Playground Series S4E1 Challenge  
- scikit-learn documentation  
