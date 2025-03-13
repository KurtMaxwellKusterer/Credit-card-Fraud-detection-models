**Credit Card Fraud Detection**

We perform a credit card fraud dection analysis based on 284,807 transactions. 

The dataset consists solely of numerical input variables derived from a **PCA transformation**.  

Due to confidentiality constraints, the original features and additional background information about the data are not provided.  

- **Features V1, V2, ... V28** represent the principal components obtained through **PCA**.  
- **Time and Amount** are the only features that were not transformed:  
  - **Time**: Represents the elapsed seconds between each transaction and the first transaction in the dataset.  
  - **Amount**: Indicates the transaction amount, which can be used for **cost-sensitive learning** based on transaction value.  
- **Class**: The target variable, where **1 indicates fraud** and **0 represents a non-fraudulent transaction**.

**Models Used**  

1. **Random Forest**  
   - A robust ensemble learning method that combines multiple decision trees.  
   - Achieved an AUC score of **0.85**, demonstrating strong classification ability.  

2. **AdaBoost**  
   - A boosting algorithm that enhances weak learners sequentially.  
   - Achieved an AUC score of **0.83**, showing competitive performance.  

3. **XGBoost**  
   - An optimized gradient boosting algorithm known for efficiency and accuracy.  
   - Achieved **98.03% accuracy**, outperforming other models.  

4. **LightGBM**  
   - A gradient boosting framework optimized for speed and memory efficiency.  
   - Achieved **95.07% accuracy**, making it a strong alternative to XGBoost.  

Model Evaluation  

- **Cross-Validation**: Applied **5-fold cross-validation (KFolds)** to ensure reliability.  
- **Final AUC Score**: **0.9756**, confirming strong predictive power.  
- **Addressing Class Imbalance**: Techniques like **SMOTE** and class weighting were considered to prevent bias toward the majority class.  

Conclusion  

The models demonstrate high performance in detecting fraudulent transactions, with **XGBoost and LightGBM** leading in accuracy. Further improvements could include hyperparameter tuning and additional feature engineering.  
