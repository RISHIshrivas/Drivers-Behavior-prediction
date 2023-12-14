# Drivers-Behavior-prediction

The Drivers Behavior Prediction project aims to develop a predictive model that analyzes and predicts the behavior of drivers based on various factors. 
By leveraging advanced data analytics and machine learning techniques, this project seeks to enhance our understanding of driver behavior and contribute to the development of intelligent systems for road safety, traffic management, and personalized driving experiences.
# the main agenda 
The code performs data loading, preprocessing, feature engineering, model training, and evaluation for a motion classification task using LightGBM. The task involves predicting the motion class ('AGGRESSIVE', 'NORMAL', 'SLOW') based on motion sensor data. The classification reports provide detailed metrics for model performance on each class.
# Data Loading and Visualization
- Import necessary libraries (e.g., os, numpy, pandas, matplotlib, seaborn, etc.).
- Upload motion data CSV files (train_motion_data.csv and test_motion_data.csv) using Google Colab.
- Create subplots for visualizing motion data (AccX) in training and test sets using Plotly.
# Data Preprocessing
- Sample and shuffle the training and test data.
- Display sample rows from both datasets.
# Data Labeling
- Create a mapping for class labels ('AGGRESSIVE', 'NORMAL', 'SLOW') to numerical values.
- Map the 'Class' column in the training dataset using the created mapping.
- Display unique class labels and the corresponding mapping.
# Data Transformation
- Create dummy variables for the 'Class' column in the training dataset.
- Concatenate the dummy variables with the original training dataset.
- Repeat the process for the test dataset.
# Data Splitting
Define target labels and split the data into features (trainX and testX) and labels (trainY and testY).
# Feature Engineering
- Define a list of columns (df_columns) for feature creation.
- Implement a timer class (Timer) for tracking time during feature creation.
- Define a function (create_numeric_feature) to create numeric features from the input data.
- Use the to_feature function to create numeric features for both training and test datasets.
# Model Training
- Define LightGBM parameters.
- Loop through each target label, perform 5-fold cross-validation, and train LightGBM models.
- Display the Root Mean Squared Logarithmic Error (RMSLE) for each fold and the overall score.
# Model Evaluation
- Convert target labels to a DataFrame (ydf).
- Loop through each target label, perform 5-fold cross-validation, train LightGBM models, and visualize feature importances.
- Display the RMSLE for each fold and the overall score.
# Model Prediction and Evaluation
- Generate predictions on the test set and visualize feature importances.
- Evaluate the model using classification reports for each target label ('AGGRESSIVE', 'NORMAL', 'SLOW').
# Usage
To use the Drivers Behavior Prediction system, follow these steps:
- Install the required dependencies (provide a list in the documentation).
- Load the pre-trained model or train a new model using the provided datasets.
- Input new data to predict driver behavior.
- Analyze the results and insights provided by the system.
# Contributing
Contributions are welcome! If you have ideas for improvements, new features, or bug fixes, please submit a pull request. For major changes, please open an issue to discuss the proposed changes.  
# License
This project is licensed under the MIT License, which means you are free to use, modify, and distribute the code for both commercial and non-commercial purposes.
