# Minimizing Churn Subscription
This repository contains code and insights on minimizing churn in a subscription-based service. The analysis is performed using a Jupyter Notebook.

## Objective
The primary objective is to predict and minimize the churn rate by analyzing various features and employing machine learning models.

## Contents
### Importing Libraries and Data
The notebook begins with importing essential libraries like Pandas, NumPy, Matplotlib, Seaborn, and reads the churn dataset using Pandas.

### Cleaning the Dataset
The dataset is explored using df.head(), df.columns, and df.describe() to understand its structure and characteristics. The cleaning process involves handling missing values by dropping columns with a significant number of NULLs and removing rows with NULLs in specific columns.

### Visualizing the Data
1. Histograms: Visualizes the distribution of numerical columns in the dataset.
2. Pie Charts: Illustrates the distribution of binary columns to assess skewness.
3. Correlation Plot and Matrix: Evaluates correlation among features using heatmap and correlation values.

### Data Preprocessing
1. One-Hot Encoding: Converts categorical variables into numerical format, avoiding the dummy variable trap.
2. Train-Test Split: Divides the dataset into training and testing sets.
3. Feature Scaling: Converts all numerical values to the range (-3,3).

### Model Building
The logistic regression model is built and trained using the training dataset.

