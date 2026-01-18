# 🚀 How to Run the Pipeline

This project follows a structured 5-step pipeline, from raw EMS eye-tracking data to machine-learning classification.

---

## **Step 1 — Data Cleaning**
**File:** `Data_Cleaning.ipynb`

This notebook performs:
- Loading raw EMS fixation data  
- Removing invalid records (blinks, zero-duration, missing pupil size)  
- Exporting cleaned fixations to: clean_data.csv


👉 **Run all cells sequentially.**

---

## **Step 2 — Exploratory Visualization**
**File:** `Data_Visualization.ipynb`

This notebook generates:
- Fixation scatter plots  
- Fixation-duration distributions  
- Heatmaps for HC vs SZ  
- Behavioural boxplots (fixations, saccades, pupil metrics)


---

## **Step 3 — Feature Extraction**
**File:** `Feature_Extraction.ipynb`

This notebook computes subject-level behavioural features:
- Fixation duration metrics  
- Saccade amplitude and saccade count  
- Spatial spread of fixations  
- Entropy & compactness  
- Pupil size variability  

👉 These features form the base dataset for machine learning.

---

## **Step 4 — Feature Selection**
**File:** `Feature_Selection.ipynb`

This notebook includes:
- Mutual Information ranking  
- PCA loading analysis  
- Correlation-based pruning  

Final output dataset: EMS_FEATURES_FINAL.csv

👉 This file is **the official input** for machine-learning models.

---

## **Step 5 — Machine Learning**
**File:** `Model.ipynb`

This notebook:
- Loads `EMS_FEATURES_FINAL.csv`
- Splits data into train/test sets  
- Trains four models:
  - Logistic Regression  
  - SVM  
  - Random Forest  
  - LDA classifier  
- Evaluates models using accuracy, confusion matrix, and decision boundary plots  

Final printed results include:
- Accuracy of each classifier  
- Identification of the best-performing model  
- Explanation of misclassification patterns  

---

## ✅ Pipeline Summary
| Step | Notebook | Output |
|------|----------|---------|
| 1 | `Data_Cleaning.ipynb` | `clean_fixations.csv` |
| 2 | `Data_Visualization.ipynb` | visualizations (scatter, density, heatmaps) |
| 3 | `Feature_Extraction.ipynb` | feature table per subject |
| 4 | `Feature_Selection.ipynb` | `EMS_FEATURES_FINAL.csv` |
| 5 | `Model.ipynb` | model accuracy + evaluation |

---
