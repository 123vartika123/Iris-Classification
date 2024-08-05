# Iris-Classification
This project uses the Iris dataset to classify flower species with a Random Forest model, including data analysis, feature scaling, model training, and hyperparameter tuning.


## Objective:
The goal of this project is to classify iris flower species using the Iris dataset. This involves a full machine learning workflow, from data exploration and preparation to model training, evaluation, and optimization.

1. Data Collection:
The Iris dataset, introduced by Ronald A. Fisher, is used. It contains 150 samples of iris flowers, with measurements for sepal length, sepal width, petal length, and petal width for three species: Iris-setosa, Iris-versicolor, and Iris-virginica.

2. Exploratory Data Analysis (EDA):

Data Inspection: Initial inspection of the dataset includes displaying the first few rows, checking the data types, and summarizing statistics.
Visualization: Pair plots are used to visualize relationships between features and explore class separability.
3. Data Cleaning:

Missing Values Check: The dataset is checked for missing values. The Iris dataset is clean and doesn’t have missing values, so no imputation is required.
4. Feature Engineering:

Standardization: Features are standardized using StandardScaler to ensure all features contribute equally to the model. This step scales the features to have zero mean and unit variance.
5. Data Splitting:

Training and Testing Sets: The dataset is split into training (70%) and testing (30%) sets to evaluate model performance.
6. Model Selection:

Random Forest Classifier: A Random Forest model is chosen for its effectiveness in handling classification tasks and providing feature importance. It aggregates the results from multiple decision trees to improve classification accuracy.
7. Model Training:

Training: The Random Forest model is trained using the training set.
8. Hyperparameter Tuning:

Grid Search: GridSearchCV is used to find the optimal hyperparameters for the Random Forest model, including n_estimators, max_features, max_depth, and criterion. The best parameters found are:
Criterion: entropy
Max Depth: 4
Max Features: log2
Number of Estimators: 50
9. Model Evaluation:

Performance Metrics: The best model is evaluated on the test set:
Confusion Matrix: Shows perfect classification with no misclassifications.
lua
Copy code
[[19  0  0]
 [ 0 13  0]
 [ 0  0 13]]
Classification Report: All metrics (precision, recall, F1-score) are 1.00, indicating flawless performance.
markdown
Copy code
              precision    recall  f1-score   support
   0       1.00      1.00      1.00        19
   1       1.00      1.00      1.00        13
   2       1.00      1.00      1.00        13
Accuracy: The model achieves 100% accuracy on the test set.
10. Cross-Validation:

Scores: Cross-validation is performed to evaluate the model's stability across different subsets of the dataset.
Scores: [0.96666667, 0.96666667, 0.93333333, 0.96666667, 1.0]
Mean Score: 0.9666666666666668, showing high performance consistency.
11. Improvement and Future Work:

Model Exploration: Consider experimenting with other models such as Support Vector Machines, Gradient Boosting, or Neural Networks.
Feature Engineering: Explore further feature engineering or selection techniques to possibly enhance performance.
Additional Hyperparameter Tuning: Continue refining hyperparameters for potential improvements.

## Summary:
This project demonstrates a complete machine learning workflow using the Iris dataset. It includes data preparation, model training with hyperparameter tuning, and thorough evaluation. The Random Forest model performs exceptionally well, achieving 100% accuracy on the test set and a high average cross-validation score. Further improvements could involve exploring different models and additional fine-tuning.
