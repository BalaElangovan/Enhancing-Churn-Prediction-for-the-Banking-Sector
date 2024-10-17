# Enhancing-Churn-Prediction-for-the-Banking-Sector


## Overview

This project focuses on developing a machine learning-based churn prediction model for the banking sector. By identifying key factors driving customer churn, the model helps banks implement targeted retention strategies. The project addresses the challenge of class imbalance using advanced techniques such as Synthetic Minority Over-sampling Technique (SMOTE) and evaluates multiple machine learning models, including Random Forest, Logistic Regression, and XGBoost.

Key goals:
- Predict customer churn using machine learning models.
- Address class imbalance in the dataset to improve model performance.
- Identify key features driving customer churn to inform business strategies.

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)

## Dataset

The dataset used in this project was sourced from Kaggle and contains customer data from a bank, including customer demographics, account details, and whether they churned. Key features include:
- CreditScore
- Geography
- Age
- Balance
- Number of Products
- IsActiveMember
- EstimatedSalary

The target variable is `Exited`, which indicates whether a customer has churned (1) or not (0).

## Methodology

### Data Preprocessing
1. **Cleaning**: Unnecessary columns such as `RowNumber` and `CustomerId` were removed to simplify the dataset.
2. **Encoding**: Categorical features such as `Geography` and `Gender` were encoded using one-hot encoding.
3. **Scaling**: Numerical features were standardized to improve the performance of machine learning algorithms.
4. **Class Imbalance**: SMOTE was applied to balance the minority class (churned customers).

### Model Development
- **Random Forest**: An ensemble learning method that builds multiple decision trees.
- **Logistic Regression**: A linear model for binary classification.
- **XGBoost**: A gradient boosting framework, known for its performance on classification tasks.

### Model Evaluation
- **Accuracy**: Measures how well the model correctly predicts churn.
- **ROC AUC**: Used to evaluate the model’s ability to distinguish between churned and non-churned customers.
- **Precision, Recall, F1-Score**: Performance metrics that provide insight into how well the model handles imbalanced data.

## Results

- **Best Model**: The Random Forest model achieved the highest performance with an ROC AUC score of **0.8494** and an accuracy of **85%**.
- **Key Features**:
  - **Age**: Older customers were more likely to churn.
  - **Number of Products**: Customers with more products were less likely to churn.
  - **Balance**: Higher account balances correlated with lower churn rates.

Visualizations of feature importance and ROC curves are available in the notebooks.

## Installation

1. Clone this repository:
```bash
git clone https://github.com/BalaElangovan/Enhancing-Churn-Prediction-for-the-Banking-Sector
```

2. Navigate to the project directory:

  ```bash
  cd Churn_Prediction_Project
  ```

3. Install the required dependencies:
  ```bash
  pip install -r requirements.txt
  ```

## Usage

To run the model training and evaluation:

```bash
  python scripts/model_training.py
```

Alternatively, open the Jupyter notebooks in the notebooks/ directory to view step-by-step data analysis and model development.

## Contributing
Contributions are welcome! Please fork the repository and create a pull request for any enhancements or fixes.
