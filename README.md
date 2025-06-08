# 📊 Customer Churn Prediction using Decision Tree with Post-Pruning

## 🧠 Overview

This project focuses on predicting **customer churn** in a telecom company using a **Decision Tree Classification** algorithm. The goal is to determine whether a customer is likely to leave the service based on demographic and behavioral attributes.  
To enhance model performance and reduce overfitting, **Cost Complexity Post-Pruning** is applied to the decision tree.

---

## 🔍 Problem Statement

Telecom companies face high churn rates, resulting in significant revenue loss. Early identification of potential churners allows companies to take proactive retention measures.  
This project builds a machine learning model to predict customer churn using historical data and improves the model using pruning techniques.

---

## 🗂️ Dataset

**Dataset Name:** Telco Customer Churn  
**Source:** [Kaggle - Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn)  
**File Used:** `WA_Fn-UseC_-Telco-Customer-Churn.csv`

---

## ⚙️ Tech Stack

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

## 🔄 Workflow

### 1. Load and Explore Dataset
- Read the CSV file using Pandas.
- Perform initial data exploration and data type correction.

### 2. Data Preprocessing
- Convert categorical variables using Label Encoding.
- Handle missing or incorrect values (e.g., in `TotalCharges`).
- Encode target column `Churn` as binary.

### 3. Train-Test Split
- Split the dataset into training and testing sets using `train_test_split()` with stratification.

### 4. Model Building
- Train a base **Decision Tree Classifier** without pruning.
- Evaluate the model using accuracy, confusion matrix, and classification report.

### 5. Post-Pruning (Cost Complexity Pruning)
- Use `cost_complexity_pruning_path()` to extract effective alpha values.
- Train multiple trees with different `ccp_alpha` values.
- Plot train and test accuracy against `ccp_alpha`.

### 6. Model Selection and Final Evaluation
- Select the optimal `ccp_alpha` based on highest test accuracy.
- Retrain the model with the selected alpha.
- Evaluate pruned model and compare with the base model.

---

## 📊 Evaluation Metrics

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Confusion Matrix**

---

## ✅ Results

- **Base Model Accuracy (Before Pruning):** ~0.7249  
- **Final Model Accuracy (After Pruning):** ~0.7860 Improved generalization, reduced overfitting.

---

## 📌 Conclusion

- Decision Tree is a powerful but overfitting-prone algorithm.
- Using **cost complexity post-pruning** improved the model's ability to generalize to unseen data.
- This approach can be easily adapted to other classification problems in business contexts.

---
