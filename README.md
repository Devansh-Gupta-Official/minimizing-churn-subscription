# Minimizing Churn Subscription
This repository contains code and insights on minimizing churn in a subscription-based service. The analysis is performed using a Jupyter Notebook.

## Objective
The primary objective is to predict and minimize the churn rate by analyzing various features and employing machine learning models. Subscription products are the main source of revenue for companies across all industries. To retain their customers, these cmpanies need to identify behavioral patterns that act as catalyst in disengagement with the product.

## Business Challenge
We will be working for a company that provides a subscription product to its users, which allows them to manage their bank accounts, provides them with personlized coupons, educates them on the best available method to save money, etc.

**We are in charge of identifying users who are likely to cancel their subsciption so that we can start building new features that they may be interested in. These features can increase the engagement and interest of our users towards the product.**

## Data
By subscribing, customers have provided data on their fijnances, and also some demographic information that was acquired during the sign-up process.

Financial data can be unreliable and delayed. Therefore, we will use only the demographic data that is built by companies.

## Contents
### Importing Libraries and Data
The notebook begins with importing essential libraries like Pandas, NumPy, Matplotlib, Seaborn, and reads the churn dataset using Pandas.

### Cleaning the Dataset
The dataset is explored using df.head(), df.columns, and df.describe() to understand its structure and characteristics. The cleaning process involves handling missing values by dropping columns with a significant number of NULLs and removing rows with NULLs in specific columns.

### Visualizing the Data
1. Histograms: Visualizes the distribution of numerical columns in the dataset.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/24359a24-191e-4520-a0a3-4110bdcfd367)


3. Pie Charts: Illustrates the distribution of binary columns to assess skewness.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/d5a906b4-519b-4186-883a-cdaa6c565ff3)


5. Correlation Plot and Matrix: Evaluates correlation among features using heatmap and correlation values.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/c2cb64ec-f666-4876-8c57-d1ba4494eee2)

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/10a59c72-9271-4680-b647-055d58bc9f82)



### Data Preprocessing
1. One-Hot Encoding: Converts categorical variables into numerical format, avoiding the dummy variable trap.
2. Train-Test Split: Divides the dataset into training and testing sets.
3. Feature Scaling: Converts all numerical values to the range (-3,3).

### Model Building
The logistic regression model is built and trained using the training dataset.
- The logistic regression model is employed for predicting churn. In this step, the model is trained using the training dataset. The LogisticRegression class from the sklearn.linear_model module is utilized, and the training data (X_train and y_train) is passed to the fit method.
- The random_state parameter is set for reproducibility. This ensures that the same initial random state is used in each run for consistent results.
- Once the model is trained, predictions are made on the test dataset (X_test). The predict method is used to obtain the predicted churn values.

### Evaluating Results
- Confusion Matrix: A confusion matrix is generated to visualize the model's performance. The confusion_matrix function from sklearn.metrics is employed for this purpose. The resulting confusion matrix is displayed using Seaborn's heatmap.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/5f696f4b-e6b7-47a3-8490-0342dfe90f9f)


- Other Scores: Calculates accuracy, precision, recall, and F1-score to evaluate the model's performance.

### Improving the Model
- K-Fold Cross-Validation: Utilizes cross-validation to improve model robustness.
- Feature Selection: Uses RFE (Recursive Feature Elimination) to select the most significant features for model training.

### Finalizing the Model
1. Rebuilds the model with the selected features and re-evaluates its performance.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/5ae083c4-2e57-4ce6-bdd2-f80218a9f323)


3. Provides insight into the most impactful features for the model.

## Results
A DataFrame ('final') containing the actual churn, predicted churn, and user information is presented for further analysis or utilization.

![image](https://github.com/Devansh-Gupta-Official/minimizing-churn-subscription/assets/100591612/6f47e523-ed19-4522-ab5d-b0ba57004581)


The notebook demonstrates steps to handle data, preprocess, build, evaluate, and optimize a machine learning model to predict and minimize churn in a subscription-based service.
