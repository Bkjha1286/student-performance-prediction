# Project Report — Student Performance Prediction

## Objective
Predict student final grade (G3) and whether a student passes (G3 >= 10) using socio-demographic and school-related features from the UCI Student Performance dataset.

## Dataset
Source: UCI Machine Learning Repository — Student Performance dataset (student-mat.csv).
Features include demographic, social, school support, and previous grades (G1, G2).

## Approach
1. Exploratory data analysis to inspect distributions and correlations.
2. Preprocessing: map binary yes/no features to 0/1, one-hot encode categorical variables.
3. Train/test split and scaling for linear/logistic models.
4. Models:
   - Regression: Linear Regression baseline, Random Forest with GridSearch.
   - Classification: Logistic Regression, Random Forest Classifier with GridSearch.
5. Evaluate with appropriate metrics (MAE, RMSE, R2 for regression; accuracy, classification report, confusion matrix for classification).
6. Save best models.

## Key Findings
- Previous grades (G1, G2) are strong predictors of final grade.
- Random Forest provides robust performance for both regression and classification.
- For early prediction (without G1, G2), model performance drops — realistic for intervention systems.

## Recommendations
- Use explainability (SHAP) to understand which features drive predictions — useful when communicating with educators.
- Deploy a Streamlit or Flask app to let users interact and run predictions on new student data.
- Expand featureset to include attendance and socio-economic variables where possible.

## Appendix
- Notebook contains code to reproduce all experiments and to save the trained models.
