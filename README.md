# 💊 Drug Interaction Severity Prediction (Project 3)

## 📌 Overview
This project demonstrates how **machine learning** can be applied in **pharmacology** to predict the severity of drug-drug interactions (DDIs).  
It is part of my **AI + Pharmacology portfolio**, showing how domain expertise and prompt engineering can be combined with machine learning workflows.

The model predicts whether an interaction is **Low**, **Moderate**, or **High** severity based on drug names and interaction descriptions.

---

## 📂 Dataset
- Source: A **balanced, synthetic dataset** of 20 drug pairs with known interactions.  
- Features:
  - `Drug1`  
  - `Drug2`  
  - `Interaction` (short text description)  
- Target:
  - `Severity` (Low, Moderate, High)  

Example rows:

| Drug1       | Drug2         | Interaction                          | Severity  |
|-------------|--------------|--------------------------------------|-----------|
| Paracetamol | Ibuprofen    | No major interaction                 | Low       |
| Warfarin    | Aspirin      | Increases bleeding risk              | High      |
| Digoxin     | Riboflavin   | May reduce absorption of Digoxin     | Moderate  |

---

## ⚙️ Workflow
The notebook covers the **end-to-end ML pipeline**:

1. **Manual CSV Upload** in Colab.  
2. **Data Cleaning** (duplicates, formatting, labels).  
3. **Exploratory Data Analysis (EDA)**:
   - Severity distribution bar chart  
   - Missing values check  
4. **Feature Engineering**:
   - Combined drug names + interaction text  
   - TF-IDF vectorization  
5. **Train / Validation / Test Split** (with stratification).  
6. **Models Trained**:
   - Logistic Regression  
   - Decision Tree Classifier  
7. **Evaluation**:
   - Accuracy on validation and test sets  
   - Classification reports  
   - Confusion matrices (heatmaps)  
   - Model comparison bar chart  
8. **Interactive Demo**:
   - Predict severity for any new drug-drug pair.  

---

## 📊 Results
- Both models worked on the small dataset.  
- Logistic Regression generalized better with text features.  
- Decision Trees were interpretable but prone to overfitting.  

**Sample Output:**

Predicted Severity for Warfarin + Aspirin: High
