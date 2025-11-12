# 🎓 Student Performance Prediction

This project analyzes student academic performance and builds predictive models to estimate final grades based on multiple factors such as demographic, social, and academic attributes. The goal is to identify the most significant features influencing performance and help educators make data-driven decisions.

---

## 🧠 Project Overview

The notebook explores the **Student Performance dataset** to:

- Perform data cleaning and preprocessing  
- Conduct exploratory data analysis (EDA) using visualizations  
- Build and evaluate machine learning models for grade prediction  
- Compare regression and classification approaches  
- Save and reuse trained models for future predictions  

---

## ⚙️ Features

- Data loading and preprocessing  
- Correlation analysis using heatmaps  
- Feature scaling and encoding  
- Model training:  
  - **Random Forest Regressor** (for predicting numeric grades)  
  - **Random Forest Classifier** (for predicting pass/fail or grade categories)  
- Model evaluation using metrics like MAE, MSE, R², accuracy, and confusion matrix  
- Model saving with `joblib` for deployment  

---

## 🧩 Tech Stack

**Language:** Python  
**Libraries:**
- pandas  
- numpy  
- matplotlib  
- seaborn  
- scikit-learn  
- joblib  

---

## 📊 Dataset

The dataset includes attributes like:

- **Demographic data:** gender, age, parental education, etc.  
- **Academic performance:** study time, failures, absences, grades (G1, G2, G3)  
- **Behavioral factors:** internet usage, health, family support  

---

## 📈 Results

- Achieved high **R² score** for regression  
- **Random Forest** performed best among tested models  
- Identified strong correlations between past grades (G1, G2) and final performance (G3)  

---

## 🔮 Future Work

- Deploy model as a web app using **Streamlit** or **Flask**  
- Integrate real-time student data input for predictions  
- Apply **hyperparameter tuning** (GridSearchCV, Optuna)  
- Extend to **multi-class grade prediction**  

---

## 👨‍💻 Author
Baidyanath Kumar Jha  
MCA Graduate, AIML Specialization  
GitHub: [Bkjha1286](https://github.com/Bkjha1286)  
LinkedIn: [baidyanath-kr-jha](https://www.linkedin.com/in/baidyanath-kr-jha-175358287/)
