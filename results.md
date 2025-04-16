# 📊 Model Results Summary

In this project, various machine learning algorithms were tested to classify water quality based on chemical properties.  
To optimize model performance, multiple **feature selection methods** were applied — including RFE, SelectKBest, and importance-based ranking.  
Each model was evaluated with **different feature combinations**, and their results compared using accuracy and F1-score metrics (with a focus on class 1).  
This systematic approach allowed us to explore the strengths and weaknesses of each algorithm and identify the most robust predictive model.


This table summarizes the classification performance of various machine learning models on the water quality dataset.  
The focus metric is **F1-Score for Class 1** (unsafe water), as the dataset is slightly imbalanced.

| Model                                         | Accuracy | F1-Score (Class 1) | Feature Selection Method              |
|-----------------------------------------------|----------|--------------------|---------------------------------------|
| Decision Tree                                 | 96.16%   | 84%                | Top 16 (RFE – model.importances_)     |
| K-Nearest Neighbors (KNN)                     | 88.64%   | 11%                | SelectKBest (Top 10)                  |
| Naïve Bayes                                   | 89.54%   | 53%                | Top 8 (based on DT importances_)      |
| Support Vector Machine (SVM, linear kernel)   | 86.08%   | 45%                | All Features                          |
| Random Forest Regressor                       | 77.78%   | -                  | -                                     |
| Random Forest Classifier                      | 95.71%   | 77%                | All Features                          |
| Bagging                                       | 86.51%   | 85%                | All Features                          |
| AdaBoost                                      | 88.04%   | 42%                | All Features                          |
| XGBoost                                       | 91.12%   | 87%                | All Features                          |
| Logistic Regression                           | 87.24%   | 41%                | All Features                          |
| TensorFlow Keras                              | 97.10%   | -                  | All Features                          |
| Pipeline (StandardScaler + LogisticRegression)| 91.00%   | 47%                | All Features                          |

> *Note:*  
> - For some models, feature selection was applied using RFE, SelectKBest, or Decision Tree-based importances.  
> - The best configuration (accuracy + F1 balance) is reported per model.  
> - **Cross-validation** was used for most models. When applied, the **accuracy value shown is the mean of the cross-validation scores.**

### 🔍 Model Comparison Insights

- **TensorFlow Keras** achieved the highest overall accuracy (97.10%), but F1-score for class 1 was not evaluated.  
- **XGBoost** provided the most balanced result in terms of both accuracy (91.12%) and F1-score (87%) — making it the most robust model overall.  
- **Bagging** also performed well, achieving 85% F1-score with 86.51% accuracy.  
- **Decision Tree** and **Random Forest Classifier** followed closely with high accuracy and decent F1-scores, suggesting their strength in handling this dataset.
