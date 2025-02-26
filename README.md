# CENG463 - Machine Learning Homework 1

## Project Overview
This project implements various regression techniques on the Heart Disease dataset from the UCI Machine Learning Repository. The goal is to analyze correlations and build predictive models using Simple Linear Regression, Multiple Linear Regression, Logistic Regression, and Polynomial Regression.

## Dataset
- **Source**: [UCI Machine Learning Repository - Heart Disease Dataset](https://archive.ics.uci.edu/dataset/45/heart+disease)
- **Features**: Various medical attributes related to heart disease.
- **Target**: Presence (1) or absence (0) of heart disease.

## Implemented Tasks
### **Task 1: Data Loading and Exploration**
- Loaded dataset using `ucimlrepo`.
- Checked for missing values and handled them by filling with the mean.
- Displayed feature names and the target variable.
- **Discussion**: Minimal missing values were found and filled with the mean to maintain dataset integrity.

### **Task 2: Correlation Analysis**
- Implemented Pearson correlation function.
- Calculated correlation between each feature and the target variable.
- Filtered features with absolute correlation > 0.3.
- **Discussion**: Strongest correlation found with feature `'ca'` (correlation = 0.517). Using highly correlated features improves model accuracy.

### **Task 3: Simple Linear Regression**
- Implemented simple linear regression using the most correlated feature.
- Computed regression coefficients and generated predictions.
- Plotted regression line.
- **Discussion**: The model showed a weak fit, indicating that a single feature might not be sufficient for accurate predictions.

### **Task 4: Multiple Linear Regression**
- Implemented multiple linear regression using the top 5 most correlated features.
- Evaluated model using Mean Squared Error (MSE).
- **Discussion**: MSE for multiple regression (0.694) was lower than simple regression (1.102), proving better predictive performance with multiple features.

### **Task 5: Logistic Regression**
- Trained a logistic regression model using the top 5 correlated features.
- Split data into training and testing sets.
- Evaluated accuracy.
- **Discussion**: Model accuracy was approximately 55%, showing moderate classification ability.

### **Task 6: Polynomial Regression**
- Applied polynomial transformation (degree 2) to the most correlated feature.
- Trained a polynomial regression model.
- Evaluated performance using MSE.
- **Discussion**: MSE = 1.096. The polynomial model captured some non-linear patterns but was limited by using only one feature.

## Conclusion
- **Best Model**: Multiple Linear Regression showed the lowest error and the best fit for the data.
- **Logistic Regression** had moderate classification accuracy.
- **Polynomial Regression** captured non-linearity but wasn’t significantly better than linear models.

## License
MIT License

