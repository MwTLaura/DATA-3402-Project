![UTA-DataScience-Logo](https://github.com/user-attachments/assets/fec1b411-bda5-437a-9eb8-08a018eb84ae)

# 📚 Customer Churn Prediction - Playground Series S4E1

## 📌 One Sentence Summary

This repository holds an attempt to predict customer churn using data from the Kaggle [Kaggle Playground Series - Season 4, Episode 1](https://www.kaggle.com/competitions/playground-series-s4e1).

---

## 📋 Overview

The task, as defined by the Kaggle challenge, is to predict whether a customer will exit a bank based on their demographic and account information. 
I approached this as a binary classification task using standard machine learning models (Logistic Regression, Random Forest, Gradient Boosting).
My best model Gradient Boosting achieved a validation score of around 87%.

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



---

## 🎯 Problem Formulation

* **Input**: Cleaned and scaled customer feature matrix.
* **Output**: Churn flag (Exited: 0 = stayed, 1 = exited).
* **Models**:
    * Logistic Regression.
    * Random Forest Classifier.
    * Gradient Boosting Classifier.

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
| Logistic Regression | ~0.84          |
| Random Forest       | ~0.86          |
| Gradient Boosting   | ~0.87          |



---

## 📋 Conclusions

* Gradient Boosting performed best overall.
* Random Forest was a close second.
* Logistic Regression was decent but simpler and less powerful by a snall margin.

---

## 🚀 Future Work

* Tune hyperparameters for Random Forest and Gradient Boosting.
* Experiment with LightGBM, XGBoost, and CatBoost.
* Perform deeper feature selection and engineering.

---

## 🔁 How to Reproduce Results

1. Install required packages: `!pip install pandas, numpy, scikit-learn, matplotlib `  
2. Download `train.csv` and `test.csv` from [Kaggle Playground S4E1](https://www.kaggle.com/competitions/playground-series-s4e1)  
3. Open the notebook `churned_prediction.ipynb`  
4. Run all cells from top to bottom.  
5. The notebook saves `cleaned_train.csv` and generates `submission.csv` for Kaggle.  

---

## 🗂️ File Structure

| File              | Description                                           |
|-------------------|-------------------------------------------------------|
| `churned_prediction.ipynb` | Main notebook with all steps: preprocessing, training, evaluation, and submission |
| `cleaned_train.csv`      | Scaled and encoded training data used for modeling |
| `submission.csv`         | Final submission file for Kaggle leaderboard     |

---

## 📚 Citations

- Kaggle Playground Series S4E1 Challenge  
- scikit-learn documentation  
