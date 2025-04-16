# 💧 Water Quality Analysis

This project focuses on evaluating and classifying water quality using various machine learning algorithms.  
It includes exploratory data analysis (EDA), feature preprocessing, model training using pipelines, and evaluation using key metrics.


📘 **Notebook**: [Water_Quality_Analysis.ipynb](Water_Quality_Analysis.ipynb)

---

## 📁 Dataset

Dataset:  
🔗 [Water Quality Dataset – by mssmartypants](https://www.kaggle.com/datasets/mssmartypants/water-quality)

Features include chemical indicators and safety results.

---

## 🧠 ML Workflow

The full pipeline includes the following steps:

1. **Data Import & Preprocessing**
   - Handling missing values
   - Feature inspection and transformation
   - Scaling using `StandardScaler`

2. **Exploratory Data Analysis (EDA)**  
   - Class distribution  
   - Distribution plots and histograms  
   - Correlation heatmap

3. **Train/Test Split**
   - Dataset split into training and test sets (80/20)

4. **Model Training**
   - Algorithms tested:
     - Logistic Regression
     - K-Nearest Neighbors (KNN)
     - Decision Tree
     - Random Forest
     - SVM
     - Naïve Bayes
     - Bagging
     - AdaBoost
     - XGBoost
     - TensorFlow Keras
     - Scikit-learn Pipeline (with scaling)

5. **Evaluation Metrics**
   - Accuracy, F1-score (with focus on unsafe water classification - class 1)

---

## 📊 Results

📄 See [results.md](results.md) for a full comparison table with accuracy, F1-scores, and feature selection info.

### 🔍 Model Insights
- **TensorFlow Keras** achieved the highest accuracy (97.10%)  
- **XGBoost** provided the best overall balance of accuracy and F1-score  
- **Bagging**, **Decision Tree**, and **Random Forest** also showed strong performance
- - **KNN** and Naïve Bayes underperformed in handling the minority class

---

## 🔧 Tools & Libraries

- Python (pandas, numpy, matplotlib, seaborn)
- scikit-learn, xgboost, tensorflow.keras

---

## 👩‍💻 Author

Developed by **Sevgi Toprak Cetin**  
This project was completed as part of a course at **Douglas College** in the Computer and Information Systems program.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).
