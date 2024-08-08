# Customer-Transaction-Prediction-Banking-Institution-
Customer Transaction Prediction (Kaggle Data from a Banking Institution)


# Santander Customer Transaction Prediction

Alejandro Monroy Azpeitia, [Agosto 8]

## Project Overview
This project aims to predict which customers will make a specific transaction in the future, irrespective of the amount of money transacted. The dataset used in this project is sourced from Kaggle and provided by Santander. The project involves extensive exploratory data analysis (EDA) using PySpark with SQL-like queries to efficiently manipulate and explore data. A significant challenge addressed in this project is the binary classification problem with potentially imbalanced data.

## Dataset Description
The dataset includes several CSV files with information about customer transactions. Here are the main files used:


## Exploratory Data Analysis (EDA) with PySpark and SQL
In the EDA phase, extensive data analysis was conducted using PySpark, leveraging SQL-like queries for efficient data manipulation and exploration. The following strategies were employed:

1. **Read and Load Data**: The CSV file was read and loaded into a PySpark DataFrame.
2. **SQL-Like Queries**: Utilized PySpark's SQL capabilities to perform  data transformations and compute statistics.
3. **Data Imbalance**: Addressed the challenge of imbalanced data, where the number of positive and negative examples in the target variable differs significantly.
5. **Data Type Correction**: Corrected data types of each column for consistency and accuracy.
6. **Outlier Analysis**: Identified outliers using statistical methods and visualizations.
7. **Handling Null Values**: Analyzed posible null values.
8. **Correlation Analysis**: Used correlation matrices to identify relationships between variables.

## Model Training
A separate Jupyter notebook was used to train different models. In all of them, a PCA analysis was performed to reduce the number of columns from 200 to 79, with a percentage of explained variance bigger  than 0.8.
### XGBoost with Hyperparameter Optimization (Optuna)
- Used Optuna for hyperparameter optimization with cross-validation.
- Evaluated using AUC-ROC curves for training and testing data.
- Plotted ROC curves and visualized recall, precision, and F1-Score against different probability thresholds.
- Selected the best model and displayed the confusion matrix.



### Logistic Regression with Data Balancing
- **Undersampling**: Used to address data imbalance by decreasing the mayoriy class instances.
- **Grid Search for Hyperparameters**: Conducted using grid search to find the best parameters.
- **Evaluation**: Assessed models using ROC curves, recall, precision, and F1-Score.
-  Selected the best model and displayed the confusion matrix.

