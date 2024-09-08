# Credit-Card-Default-Prediction-Using-Machine-Learning-A-Comparative-Study-with-XGBoost-Optimization

![Credit Card Default prediction](https://github.com/rdcodings/Credit-Card-Default-Prediction-Using-Machine-Learning-A-Comparative-Study-with-XGBoost-Optimization/blob/3c28a5935835c2881a8e170c670736272f7e066d/CC.png)


### Introduction:
Credit risk represents the potential financial loss a lender or investor might incur if a borrower fails to meet their loan repayment or other financial commitments. It reflects the danger of default arising from a borrower’s inability or unwillingness to repay the borrowed funds. For banks, financial institutions, and investors, credit risk is a critical issue, as it can significantly reduce the value of their investments or, in some cases, lead to a total loss of the principal amount.

To mitigate this risk, lenders and investors rely on credit scoring models, detailed borrower assessments, and the establishment of credit limits and collateral requirements. However, traditional methods often lack the precision needed to predict defaults early and accurately. Machine learning models have become invaluable in this area, providing a data-driven approach to identifying high-risk borrowers before defaults occur.

In this project, we develop a credit risk model to predict the likelihood of a client defaulting on their credit card payment for a bank in Taiwan. Using a comparative approach, we explore various machine learning models, including XGBoost, to identify the most effective method for assessing credit risk.

### Objective:
The goal of this project is to predict the likelihood of credit card default in the upcoming month using various machine learning models. This predictive model will assist financial institutions in assessing credit risk, thereby reducing potential financial losses due to client defaults. The dataset utilized comes from a Taiwanese bank and contains information on 30,000 credit card clients.

### Methodology:
1. **Data Preprocessing**:
   - **Dataset**: The dataset contains 25 features, including demographic data (e.g., age, gender, education) and financial behavior (e.g., payment status, bill amounts).
   - **Cleaning**: Removed irrelevant features such as `ID`, and grouped unknown categories in `EDUCATION` and `MARRIAGE` for better clarity.
   - **Balancing**: The target variable (`Default`) was highly imbalanced, with 22% defaults. The SMOTE (Synthetic Minority Over-sampling Technique) algorithm was used to balance the training data.
   - **Feature Scaling**: StandardScaler was used to normalize the features before training the models.

2. **Feature Engineering and Visualization**:
   - Visualized various demographic and financial features such as `AGE`, `SEX`, and `EDUCATION` to explore their distributions and relationship with default rates.
   - Analyzed correlations between features, particularly focusing on payment status (`PAY_0` to `PAY_6`) and bill amounts.

3. **Model Development**:
   - Four machine learning models were developed and evaluated:
     1. **Logistic Regression**
     2. **Decision Tree Classifier**
     3. **Random Forest Classifier**
     4. **XGBoost Classifier**
   - Each model was trained on the balanced dataset using an 80-20 train-test split.
   - Hyperparameter tuning was applied to XGBoost using RandomizedSearchCV to further optimize its performance.

4. **Evaluation Metrics**:
   - Each model was evaluated based on **accuracy**, **precision**, **recall**, **F1-score**, and the **confusion matrix**.
   - The **ROC-AUC curves** were plotted for each model to compare their performance in distinguishing between default and non-default clients.
### Results Comparison:
1. **Logistic Regression**:  
   - **Accuracy**: 68.58%  
   - **Precision**: 0.88 (non-default), 0.38 (default)

2. **Decision Tree**:  
   - **Accuracy**: 67.32%  
   - **Precision**: 0.88 (non-default), 0.36 (default)

3. **Random Forest**:  
   - **Accuracy**: 79.63%  
   - **Precision**: 0.86 (non-default), 0.54 (default)

4. **XGBoost**:  
   - **Accuracy**: 80.42%  
   - **Precision**: 0.85 (non-default), 0.57 (default)

5. **XGBoost (with hyperparameter tuning)**:  
   - **Accuracy**: 80.55%  
   - **Precision**: 0.85 (non-default), 0.57 (default)

### Conclusion:
This project successfully demonstrated the application of machine learning models for credit card default prediction. The Random Forest and XGBoost models outperformed Logistic Regression and Decision Tree models, with XGBoost achieving the highest accuracy (80.55%) after hyperparameter tuning. While XGBoost provided the best results, its margin over Random Forest was small, suggesting both models are strong candidates for credit default prediction.

Overall, XGBoost is the recommended model for this use case due to its superior performance in terms of accuracy and precision. This model can assist financial institutions in making data-driven decisions to mitigate credit risk effectively.

Author - *Rajarshi Das*
