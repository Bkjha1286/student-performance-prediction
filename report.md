# Project Report — Student Performance Prediction

## Objective
Predict whether a student passes or fails their final exam (G3 >= 10) using socio-demographic, lifestyle, and academic features from the UCI Student Performance dataset. A binary classification target is defined: Pass (1) if G3 >= 10, Fail (0) otherwise.

## Dataset
UCI Machine Learning Repository — Student Performance dataset (student-mat.csv, student-por.csv). Features include demographic details (age, sex, address), family background (parental education and jobs), school support (schoolsup, famsup, paid), lifestyle factors (goout, Dalc, Walc, romantic, internet), and academic history (failures, absences, G1, G2).

## Approach
1.Exploratory data analysis through a 5-panel dark-theme dashboard — KPI overview (total students, pass/fail rate, average grade), grade distribution, pass rate by gender and address, risk factor analysis (failures, study time, absences, parental education, lifestyle factors), and a full Pearson correlation heatmap.

2.Preprocessing: Label Encoding applied to all categorical columns; four engineered features created — grade_trend (G2−G1), avg_parent_edu ((Medu+Fedu)/2), risk_score (failures + absences/10 + Dalc), support_score (schoolsup + famsup + paid).

3.Train/test split (80/20, stratified by target) and StandardScaler applied; same scaler used to transform test set.
Models:

4.Classification: Logistic Regression (max_iter=1000, C=1.0), Decision Tree (max_depth=5), Random Forest (n_estimators=150, max_depth=7).

5.Evaluate with accuracy, precision, recall, F1 score, AUC-ROC, confusion matrix, full classification report, and 5-Fold Stratified Cross Validation accuracy.

6.Live prediction on a new student profile using all three trained models, outputting Pass/Fail label and pass probability percentage.

## Key Findings
1.Previous grades G1 and G2 are the strongest predictors — highest Pearson correlation with G3 and top-ranked in Random Forest feature importance.

2.Engineered feature grade_trend (G2−G1) captures academic momentum and is a valuable predictor — a positive trend strongly associates with passing.

3.Students with zero past failures pass at a significantly higher rate; even one past failure causes a sharp drop in pass rate.

4.Higher study time, internet access, and higher education aspiration all positively correlate with passing; higher absences consistently associate with failure.

5.Random Forest is the best performing model with F1 ~0.92 and AUC ~0.93, outperforming both Logistic Regression and Decision Tree across all metrics.

## Recommendations
1.Apply GridSearchCV for hyperparameter tuning on Random Forest and Decision Tree to further optimise F1 score.

2.Use SHAP (SHapley Additive exPlanations) to explain individual predictions — particularly useful when communicating results to teachers and school administrators.

3.Deploy as a Streamlit or Flask web application so educators can input student details and receive real-time pass/fail predictions without any coding.

4.Build a separate early-intervention model excluding G1 and G2 to identify at-risk students before mid-term results are available — more actionable for schools.

## Appendix
Notebook contains code to reproduce all 5 EDA dashboard panels, feature engineering, model training, evaluation visualisations (grouped metric comparison, confusion matrices, ROC curves, Random Forest feature importance, Decision Tree structure up to depth 3), classification reports, and live prediction for a new student input.
