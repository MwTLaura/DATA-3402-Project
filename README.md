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

<img width="712" alt="Image" src="https://github.com/user-attachments/assets/3875d626-0eee-4fb7-9518-c09472ab3e61" />

<img width="710" alt="Image" src="https://github.com/user-attachments/assets/f48f6dcd-2c07-48a7-a17c-9efb0a365b82" /> 

<img width="709" alt="Image" src="https://github.com/user-attachments/assets/79891be5-1a84-425c-b3ca-3dba175c1189" />

<img width="705" alt="Image" src="https://github.com/user-attachments/assets/42c4c4ef-bb1f-48a1-827f-d619aa6be31c" />


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


<img width="687" alt="Image" src="https://github.com/user-attachments/assets/9ffece01-f952-4aa4-8534-51e2f30e5d76" />


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
