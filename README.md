# 🎓 Student Performance Prediction

This project analyzes student academic performance and builds machine learning classification models to predict whether a student will Pass or Fail based on demographic, lifestyle, school support, and academic features. The goal is to identify key risk factors and help educators make data-driven intervention decisions.

---

## 🧠 Project Overview

The notebook explores the **UCI Student Performance dataset** to:
- Perform exploratory data analysis through a 5-panel dark-theme dashboard
- Engineer meaningful features from raw data
- Build and evaluate three classification models for pass/fail prediction
- Compare model performance using multiple evaluation metrics
- Generate live predictions for new student profiles

---

## ⚙️ Features
- 5-panel dark-theme EDA dashboard covering KPIs, risk factors, and correlations
- Feature engineering: grade_trend, risk_score, support_score, avg_parent_edu
- Feature encoding with LabelEncoder and scaling with StandardScaler
- Model training:
  - Logistic Regression
  - Decision Tree Classifier (max_depth=5)
  - Random Forest Classifier (n_estimators=150)
- Model evaluation: Accuracy, Precision, Recall, F1, AUC-ROC, 5-Fold Cross Validation
- Visualisations: confusion matrices, ROC curves, feature importance, decision tree plot
- Live pass/fail prediction with probability scores for a new student input

---

## 🧩 Tech Stack
**Language:** Python  
**Libraries:**
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

---

## 📊 Dataset
- **Source:** UCI Machine Learning Repository — Student Performance Dataset
- **File used:** student-mat.csv (395 students, 30 features)
- **Target:** pass_fail (1 = Pass if G3 ≥ 10, 0 = Fail)
- **Feature categories:** demographic, parental background, school support, lifestyle, academic history

---

## 📈 Results
- Random Forest achieved the best performance: F1 ~0.92, AUC ~0.93
- G1 and G2 (previous grades) are the strongest predictors of final outcome
- Engineered feature grade_trend (G2−G1) proved highly informative
- Students with zero past failures pass at significantly higher rates

---

## 🔮 Future Work
- Deploy as a web app using Streamlit or Flask
- Apply GridSearchCV for hyperparameter tuning
- Add SHAP explainability to communicate predictions to educators
- Build an early-intervention model excluding G1/G2 for use before mid-terms

---

## 👨‍💻 Author
Baidyanath Kumar Jha  
MCA Graduate, AIML Specialization  
GitHub: [Bkjha1286](https://github.com/Bkjha1286)  
LinkedIn: [baidyanath-kr-jha](https://www.linkedin.com/in/baidyanath-kr-jha-175358287/)
