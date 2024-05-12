# Regression-on-Flood-Prediction
Regression with a Flood Prediction Dataset Overview Welcome to the 2024 Kaggle Playground Series! We plan to continue in the spirit of previous playgrounds, providing interesting an approachable datasets for our community to practice their machine learning skills, and anticipate a competition each month.

For my project "Flood Risk Prediction," I applied various data engineering steps and created predictive models to estimate flood probabilities. Below is a breakdown of the code with added data loading and cleaning steps:

Data Loading and Cleaning:
Load the dataset df containing features and target variable 'FloodProbability'.
Perform any necessary data cleaning steps such as handling missing values, encoding categorical variables, or removing outliers.
Model Building:
Utilize the LinearRegression model to predict flood probabilities.
Separate features X and target variable y.
Split the data into training and testing sets using train_test_split.
Train the linear regression model on the training data (X_train, y_train).
Predict flood probabilities on the test set (X_test) and calculate the R2 score using r2_score.
Utilize the DecisionTreeRegressor for cross-validated predictions.
Instantiate the model.
Perform cross-validation using cross_val_score to obtain R2 scores for each fold.
Calculate the mean R2 score across all folds.
Utilize the RandomForestRegressor for cross-validated predictions.
Instantiate the model.
Perform cross-validation and calculate the mean R2 score.
Submission Preparation:
Assuming the test_df DataFrame is loaded:
Predict 'FloodProbability' for the testing data using the trained linear regression model (model.predict(test_df)).
Create a DataFrame submission_df with columns 'id' (assuming it exists in test_df) and 'FloodProbability' containing the predicted values.
Save the DataFrame to a CSV file named 'submission.csv' without including the index.
Overall, this code snippet demonstrates the process of loading, cleaning, modeling, and preparing predictions for flood risk probabilities, utilizing linear regression, decision tree, and random forest regressors.
