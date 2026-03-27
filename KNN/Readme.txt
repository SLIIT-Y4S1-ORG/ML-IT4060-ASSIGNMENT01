#  Machine Learning Assignment – KNN Classification

##  Overview

This project focuses on predicting company bankruptcy using a real-world financial dataset.
The task is treated as a binary classification problem, where the model predicts whether a company is bankrupt (1) or not (0).

The K-Nearest Neighbors (KNN) algorithm is used as the primary model, and special attention is given to handling class imbalance using SMOTE.

---

## Dataset

* The dataset contains financial features of companies.
* Target variable: **Bankrupt?**

  * 0 → Non-bankrupt
  * 1 → Bankrupt

###  Key Challenge

The dataset is highly imbalanced:

* Majority class (0) dominates
* Minority class (1) is significantly smaller

---

## Methodology

### 1. Data Preprocessing

* Checked for missing values
* Split dataset into training and testing sets
* Applied **StandardScaler** for feature scaling

### 2. Handling Imbalance

* Applied **SMOTE (Synthetic Minority Over-sampling Technique)**
* Balanced the training dataset before model training

### 3. Model Used

* **Algorithm**: K-Nearest Neighbors (KNN)
* **K value**: 5

---

##  Results

### Before SMOTE

* Accuracy: **96.26%**

**Observation:**

* High accuracy but poor performance on minority class
* Model biased toward non-bankrupt class

---

### After SMOTE

* Accuracy: **88.81%**

**Observation:**

* Significant improvement in detecting bankrupt cases
* Better recall for minority class
* Slight increase in false positives

---

## Key Insights

* Accuracy alone is not a reliable metric for imbalanced datasets
* Recall and confusion matrix provide better understanding
* SMOTE helps improve minority class detection

---

## How to Run

1. Open Jupyter Notebook
2. Install required libraries:

   ```bash
   pip install pandas numpy scikit-learn seaborn matplotlib imbalanced-learn
   ```
3. Run the notebook step by step
4. View results and visualizations

---

## Project Structure

```
├── data.csv
├── KNN_Assignment.ipynb
├── README.md
├── report.pdf
```

---

##  Future Improvements

* Tune K value for better performance
* Try other algorithms (Decision Tree, Random Forest)
* Use advanced imbalance handling techniques
* Perform feature engineering

---

##  Contributors

* Panduka Wijesinghe

---

## Notes

* This project was developed as part of a Machine Learning assignment
* Code is provided in the notebook and included in the report appendix
