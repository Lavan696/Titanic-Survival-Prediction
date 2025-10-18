# Titanic Survival Prediction using Random Forest Classifier

This project predicts passenger survival on the **Titanic dataset** from Kaggle using a **Random Forest Classifier**.  
Since the test set provided by Kaggle lacks labels, the original train set was split into **training and testing sets** for evaluation.  
The project focuses on effective feature engineering, model tuning, and evaluation using key classification metrics and visualizations.

---

## Key Features and Steps

- ✅ Loaded the **Titanic dataset** from Kaggle.  
- ✅ Added engineered features:  
  - `FamilySize = Parch + SibSp`  
  - `FarePerPerson = Fare / FamilySize`  
- ✅ Dropped unnecessary features: `Name`, `SibSp`, `Parch`, `Ticket`.  
- ✅ Replaced missing values in `Age` with **median**.  
- ✅ Scaled numerical features using **StandardScaler**.  
- ✅ Encoded categorical variables:  
  - **Embarked** using label encoding.  
  - **Sex** replaced with 1 (male) and 0 (female).  
  - **Cabin** values encoded numerically.  
- ✅ Split dataset into **training (80%)** and **testing (20%)** sets.  
- ✅ Trained a **Random Forest Classifier** with defined hyperparameters.  
- ✅ Identified and selected **top 20 important features** based on feature importance.  
- ✅ Retrained the model using top features and re-evaluated performance.  
- ✅ Displayed **confusion matrix**, **precision-recall curve**, and **ROC curve**.  
- ✅ Tuned threshold to achieve balanced **precision ≈ recall ≈ 80%**.  
- ✅ Visualized **classification report heatmap** using Seaborn.

---
##  Results Summary
| **Cross-Val Score (Full Features)** | **81.31%** |
| 📈 Metric       | 🔢 Score |
|:-----------------------------    |:----------------:|

| **Cross-Val mean score (final)** | **81.03%** |
| **Accuracy**                     | **83.24%** |
| **Precision**                    | **80.26%** |
| **Recall**                       | **80.26%** |
| **F1 Score**                     | **80.26%** |
| **ROC-AUC Score**                | **82.85%** |

---

##  Tech Stack
- Python  
- scikit-learn  
- pandas  
- NumPy  
- Matplotlib  
- Seaborn  

---

## 📂 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/titanic-survival-prediction.git
