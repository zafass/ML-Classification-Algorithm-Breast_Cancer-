# Breast Cancer Classification with Supervised Learning

## Objective

The goal of this project is to apply supervised learning techniques to classify breast cancer cases using the dataset provided in the sklearn library. This involves evaluating the performance of multiple classification algorithms to determine the most suitable model for this dataset.

## Dataset

The breast cancer dataset from the sklearn.datasets module is used. This dataset contains 30 features related to cell nuclei characteristics, along with a target column that classifies cases as malignant (1) or benign (0).
* Number of Instances: 569
* Number of Features: 30 numerical features
* Target Classes: 2 (Malignant and Benign)

## Loading and Preprocessing
* The dataset is loaded using the load_breast_cancer function from sklearn.datasets.
* It is converted into a pandas DataFrame for easier manipulation.
* The dataset was inspected, and no missing values were found.
* Therefore, no imputation or handling was required.
* Applied StandardScaler to standardize the features to have a mean of 0 and a standard deviation of 1.
* Used MinMaxScaler to normalize features to a range between 0 and 1 for certain models that benefit from bounded inputs.

## Classification Algorithm Implementation
### Logistic Regression:
* A statistical model that predicts binary outcomes using a linear combination of features and a sigmoid function.
* Suitability: Simple yet effective for linearly separable datasets.

### Decision Tree Classifier:
* Constructs a tree where nodes represent features and splits occur based on thresholds to separate classes.
* Suitability: Captures non-linear relationships and is easy to interpret.

### Random Forest Classifier:
* An ensemble of decision trees that aggregates predictions to improve accuracy and generalization.
* Suitability: Reduces overfitting and handles non-linearity effectively.

### Support Vector Machine (SVM):
* Finds a hyperplane that maximizes the margin between two classes.
* Suitability: Effective in high-dimensional spaces.

### k-Nearest Neighbors (k-NN):
* Classifies instances based on the majority class of the nearest k neighbors.
* Suitability: Non-parametric, making it useful for smaller datasets.

## Model Comparison
### Metrics:
* Accuracy, Precision, Recall, and F1-score were used to evaluate model performance.
* Cross-validation ensured robust performance estimates.

## Conclusion

This project demonstrates the application of various supervised learning algorithms to classify breast cancer cases. The insights gained provide a basis for selecting models that balance accuracy, interpretability, and computational efficiency for medical diagnostics. The best-performing algorithm was k-NN, which achieved an accuracy of 0.973684. The least effective model was Decision Tree.
