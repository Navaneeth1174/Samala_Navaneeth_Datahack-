# Vaccine Adoption Prediction Using Machine Learning

In this project, we aim to predict the likelihood of individuals adopting two different vaccines: the xyz vaccine and the seasonal vaccine. Leveraging a dataset of demographic and survey-based features, we build a robust machine learning pipeline to preprocess the data, train predictive models, and evaluate their performance.

Objectives:

Data Integration:

Merge features and labels datasets on respondent IDs to form a comprehensive training dataset.
Data Preprocessing:

Handle missing values using appropriate imputation techniques.
Standardize numerical features to ensure uniform scaling.
Encode categorical features using one-hot encoding to facilitate their use in the model.
Model Development:

Use a RandomForestClassifier wrapped in a MultiOutputClassifier to handle multi-label classification.
Build a pipeline to streamline preprocessing and model training.
Model Evaluation:

Split the dataset into training and validation sets.
Train the model and predict probabilities on the validation set.
Evaluate model performance using the ROC AUC metric for each vaccine, and calculate the mean ROC AUC as a combined performance indicator.
Prediction and Submission:

Apply the trained model to the test dataset.
Generate predictions and create a submission file for further analysis or competition submission.
Steps and Methodology:

Data Loading and Merging:

Load the training features and labels from CSV and Excel files, respectively.
Merge the datasets on the respondent_id column to form the training dataset.
Feature Selection:

Drop irrelevant columns like respondent_id and target columns from the feature set.
Pipeline Construction:

Create separate preprocessing pipelines for numerical and categorical features.
Integrate these pipelines using a ColumnTransformer.
Model Training and Evaluation:

Split the dataset into training and validation subsets.
Fit the pipeline on the training data and evaluate it on the validation data.
Calculate ROC AUC scores for both vaccines and their mean.
Prediction and Output:

Preprocess and predict on the test dataset.
Prepare a submission file with the predicted probabilities for both vaccines.
Results:

The model achieved an ROC AUC score of 0.829 for the xyz vaccine and 0.852 for the seasonal vaccine on the validation set, with a mean ROC AUC of 0.841.
Conclusion:

This project demonstrates the effectiveness of machine learning in predicting vaccine adoption based on demographic and survey data. The pipeline approach ensures reproducibility and scalability, allowing for future improvements and adaptations to different datasets or problem settings.
