# Titanic Survival Prediction using Random Forest Classifier  

This project predicts passenger survival on the Titanic dataset using **Random Forest Classifier**.  
The dataset was taken from **Kaggle**, and the model was built using  
**Scikit-learn, Pandas, NumPy, Matplotlib, and Seaborn**.  

---

##  Project Overview  
The goal of this project is to predict whether a passenger survived the Titanic disaster based on various attributes such as age, gender, class, and more.  
Since the test set provided by Kaggle does not include labels, the original **train set was split** into training and testing sets to evaluate the model locally.

---

##  Steps Followed  

1. **Loaded the dataset** and performed initial exploration  
2. **Feature Engineering:**  
   - Added new features:  
     - `FamilySize = SibSp + Parch`  
     - `FarePerPerson = Fare / FamilySize`  
   - Dropped columns: `Name`, `SibSp`, `Parch`, and `Ticket`  
3. **Handled Missing Values:** Replaced missing values in `Age` with the median  
4. **Feature Scaling:** Scaled numerical columns using `StandardScaler`  
5. **Encoding:**  
   - Converted `Sex` column into numerical form (Male → 1, Female → 0)  
   - One-hot encoded `Embarked` column  
   - Encoded `Cabin` feature  
6. **Model Building:**  
   - Used **Random Forest Classifier** with tuned hyperparameters  
   - Evaluated with **cross-validation**  
7. **Feature Importance:**  
   - Extracted top 20 important features and retrained the model  
8. **Visualization:**  
   - Plotted **Confusion Matrix**, **Precision-Recall Curve**, **ROC Curve**, and **Classification Report Heatmap**

---

## Model Performance Comparison  

| Metric                      | Before Threshold Adjustment | After Threshold (Precision = Recall = 82%) |
|:----------------------------|:---------------------------:|:------------------------------------------:|
| Cross-Validation Mean Score | **82.02%**                  | **82.02%**                                 |
| Test Accuracy               | **83.70%**                  | **84.36%**                                 |
| Precision score             | **82.19%**                  | **81.58%**                                 |
| Recall  score               | **78.94%**                  | **81.58%**                                 |
| f1 Score                    | **80.53%**                  | **81.58%**                                 |
| ROC-AUC score               | **83.16%**                  | **83.99%**                                 |

---

##  Key Insight  

After adjusting the **classification threshold** to maintain both **precision and recall around 82%**,  
the model achieved better balance and consistency across metrics.  
While accuracy improved slightly, the overall **F1-score** and **recall** also increased, making the model more reliable.

---

##  Tech Stack  
- **Programming Language:** Python   
- **Libraries Used:**  
  - Scikit-learn  
  - Pandas  
  - NumPy  
  - Matplotlib  
  - Seaborn  

---

##  Visualizations 

- **Feature Importance (Top 20 Features)** – Bar plot  
- **Feature Correlation Heatmap** – Heatmap of top features  
- **Correlation with Target** – Bar plot of feature correlation with survival  
- **Confusion Matrix** – Before and After threshold optimization  
- **Precision-Recall Curve** – To analyze trade-off between precision and recall  
- **ROC Curve** – Receiver Operating Characteristic curve  
- **Classification Report Heatmap** – Metrics visualization for each class  
- **Pairplot** – Relationships between features (`Age`, `Fare`, `Pclass`, `Sex`) and `Survived`  
- **OOB Score Plot** – Out-of-Bag score of the Random Forest model
   
---

##  Future Improvements  
- Experiment with other ensemble methods like **XGBoost** or **Gradient Boosting** 
---

##  Dataset Source  
 [Titanic - Machine Learning from Disaster | Kaggle](https://homl.info/titanic.tgz)
---

##  Author  

**Lavan kumar Konda**  
-  Student at NIT Andhra Pradesh  
-  Passionate about Data Science, Machine Learning, and AI  
- 🔗 [LinkedIn](www.linkedin.com/in/lavan-kumar-konda)

