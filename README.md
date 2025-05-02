![UTA-DataScience-Logo](https://github.com/user-attachments/assets/fec1b411-bda5-437a-9eb8-08a018eb84ae)

# 📚 Customer Churn Prediction - Playground Series S4E1

## 📌 One Sentence Summary

This repository holds an attempt to predict customer churn using data from the Kaggle [Kaggle Playground Series - Season 4, Episode 1](https://www.kaggle.com/competitions/playground-series-s4e1).

---

## 📋 Overview

This project focuses on predicting customer churn based on structured banking data, as defined in the Kaggle Playground Series Season 4, Episode 1 competition. The goal is to determine whether a customer is likely to exit the bank based on their demographic and account-related features.
The problem is approached as a binary classification task, where the target variable indicates whether the customer exited (1) or not (0). The dataset includes a mix of numerical and categorical features such as credit score, geography, age, balance, and account activity status.
The full machine learning pipeline was implemented in a single notebook. It includes data cleaning, feature scaling, one-hot encoding, data visualization, model training, and evaluation using multiple classifiers (Logistic Regression, Random Forest, Gradient Boosting). ROC AUC was used as the main evaluation metric, consistent with the competition’s scoring method.
My best-performing model, Gradient Boosting, achieved an AUC of approximately 89% and an accuracy score of around 87%. This suggests good generalization and strong model performance relative to baseline approaches.

---

## 📂 Data

* **Type**: CSV file with customer features and binary churn flag (Exited).
* **Size**: 165,034 samples for training.
* **Train/Validation/Test Split**:
    * 60% training.
    * 20% validation.
    * 20% testing.

---

## 🛠️ Preprocessing

- **Dropped**: `id`, `CustomerId`, `Surname`.
- Scaled numerical features using **StandardScaler**.
- **One-hot** encoded `Geography` and `Gender`.
- No missing or duplicate values.

---

## 📊 Data Visualization

**Categorical Features**

<img width="712" alt="Image" src="https://github.com/user-attachments/assets/3875d626-0eee-4fb7-9518-c09472ab3e61" />

**Important Features Scaled**

<img width="1001" alt="Image" src="https://github.com/user-attachments/assets/dc75f5f5-cbd5-4591-8a8e-849c2529057e" />


---

## 🎯 Problem Formulation

* **Input**: Cleaned and scaled customer feature matrix.
* **Output**: Churn flag (Exited: 0 = stayed, 1 = exited).
* **Models**:
    * Logistic Regression.
    * Random Forest Classifier.
    * Gradient Boosting Classifier.
* **Metric**: AUC.

---

## 🏋️ Training

* **Software**: Python 3, scikit-learn, Jupyter Notebook - Anaconda.
* **Hardware**: Standard Mac CPU.
* **Training Time**: A few minutes per model.
* **Stopping Criteria**: No manual stopping needed.

---

## 📈 Performance Comparison

| Model               | Validation AUC |
|---------------------|----------------|
| Logistic Regression | ~0.82          |
| Random Forest       | ~0.87          |
| Gradient Boosting   | ~0.89          |


<img width="687" alt="Image" src="https://github.com/user-attachments/assets/9ffece01-f952-4aa4-8534-51e2f30e5d76" />


---

## 📋 Conclusions

* Gradient Boosting performed best overall.
* Random Forest was a close second.
* Logistic Regression was decent but simpler and less powerful.

---

## 🚀 Future Work

* Tune hyperparameters for Random Forest and Gradient Boosting.
* Experiment with LightGBM, XGBoost, and CatBoost.
* Perform deeper feature selection and engineering.

---

## 🔁 How to Reproduce Results

1.  Download `train.csv` and `test.csv` from [Kaggle Playground S4E1](https://www.kaggle.com/competitions/playground-series-s4e1)  
3. Open the notebook `churned_prediction.ipynb`
4. Install required packages: `!pip install pandas, numpy, scikit-learn, matplotlib `  
5. Run all cells from top to bottom.  
6. The notebook saves `cleaned_train.csv` and generates `submission.csv` for Kaggle.  

---

## 🗂️ File Structure

| File              | Description                                           |
|-------------------|-------------------------------------------------------|
| `churned_prediction.ipynb` | Main notebook with all steps: preprocessing, training, evaluation, and submission |
| `cleaned_train.csv`      | Scaled and encoded training data used for modeling |
| `submission.csv`         | Final submission file for Kaggle leaderboard     |

---

## 📚 Citations

- Kaggle Playground Series S4E1 Challenge: https://www.kaggle.com/competitions/playground-series-s4e1  
- scikit-learn documentation: https://scikit-learn.org/stable/
