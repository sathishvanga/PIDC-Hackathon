# PIDC-Hackathon

# Customer Churn Prediction

This project, developed by Sathish Vanga, aims to predict customer churn for a telecommunications company. By leveraging various data factors such as customer demographics, usage patterns, billing history, and customer service interactions, the goal is to create a predictive model to identify customers likely to churn, enabling targeted retention strategies.

## Table of Contents
- [Business Understanding](#business-understanding)
- [Data Understanding](#data-understanding)
- [Data Preparation and Engineering](#data-preparation-and-engineering)
- [Model Building](#model-building)
- [Model Evaluation](#model-evaluation)
- [Conclusion and Recommendation](#conclusion-and-recommendation)
- [Deployment](#deployment)

## Business Understanding
### Problem Statement
Develop a predictive model to estimate the likelihood of customer churn for a telecommunications company. The model should consider various factors such as customer demographics, usage patterns, billing history, and customer service interactions.

### Objective
Build a predictive model that accurately identifies customers likely to churn. This helps the telecommunication company implement targeted retention strategies to reduce churn rates, enhance customer satisfaction, and improve overall profitability.

## Data Understanding
- Described the dataset columns and their meanings.
- Checked for missing values and duplicated records, ensuring no missing and duplicate values.
- Verified data types of columns and corrected issues such as incorrect data types (e.g., 'TotalCharges').
- Conducted exploratory data analysis (EDA) to gain insights into the dataset's characteristics, including statistical summaries and visualizations.

## Data Preparation and Engineering
### Exploratory Data Analysis
- Conducted statistical analysis on key numerical features like tenure, MonthlyCharges, and TotalCharges.
- Visualized distributions and relationships between variables using various plots.
- Performed hypothesis testing to understand the association between variables and churn.

### Data Cleaning
- Handled missing values in the 'TotalCharges' column by replacing them with the median.
- Grouped related service columns into a single feature to reduce dimensionality.
- Transformed categorical variables into binary features for better modeling.

## Model Building
- Split the dataset into training (75%) and testing (25%) sets.
- Used StandardScaler to normalize numerical features.
- Applied OneHotEncoder for binary categorical features and OrdinalEncoder for multi-class categorical features.
- Created a preprocessing pipeline to ensure consistency and efficiency in data preparation.

## Model Evaluation
### Evaluation Metrics
Each model's performance was evaluated using:
- **Accuracy**: The proportion of correctly classified instances.
- **F1 Score**: The harmonic mean of precision and recall.
- **Recall**: The proportion of actual positives correctly identified.
- **Precision**: The proportion of positive identifications that are actually correct.
- **Confusion Matrix**: A table showing true positive, true negative, false positive, and false negative predictions.
- **Classification Report**: Detailed metrics for each class, including precision, recall, and F1 score.

### Results
#### Logistic Regression
- **Accuracy**: 80.8%
- **F1 Score**: 80.2%
- **Recall**: 80.8%
- **Precision**: 80.4%
- **Confusion Matrix**:
  - True Negatives: 1100
  - False Positives: 227
  - False Negatives: 201
  - True Positives: 372

#### SGD Classification
- **Accuracy**: 80.9%
- **F1 Score**: 80.1%
- **Recall**: 80.9%
- **Precision**: 80.5%
- **Confusion Matrix**:
  - True Negatives: 1111
  - False Positives: 216
  - False Negatives: 186
  - True Positives: 387

#### Decision Tree Classification
- **Accuracy**: 75.5%
- **F1 Score**: 74.2%
- **Recall**: 75.5%
- **Precision**: 74.8%
- **Confusion Matrix**:
  - True Negatives: 999
  - False Positives: 328
  - False Negatives: 168
  - True Positives: 405

#### Random Forest Classification
- **Accuracy**: 80.5%
- **F1 Score**: 79.7%
- **Recall**: 80.5%
- **Precision**: 79.9%
- **Confusion Matrix**:
  - True Negatives: 1101
  - False Positives: 226
  - False Negatives: 207
  - True Positives: 366

## Conclusion and Recommendation
The SGD Classifier achieved the highest accuracy (80.9%) and balanced performance across other metrics. The Logistic Regression model also performed well with an accuracy of 80.8%. The Decision Tree Classifier had the lowest performance with an accuracy of 75.5%, while the Random Forest Classifier demonstrated good performance but had a larger model size.

**Recommendation**: Based on the evaluation metrics, the SGD Classifier is recommended for deployment due to its high accuracy, efficient model size, and balanced performance. The Logistic Regression model is a close second and can be considered as an alternative, especially if model interpretability is important.

## Deployment
A Streamlit application was developed to predict customer churn for a telecommunications company based on various input features. The application utilizes a trained machine learning model to make predictions.

### Steps to Interact with the Application
1. **Input Features**: Provide necessary information about the customer demographics, usage patterns, billing history, and service interactions.
2. **Click on Predict**: After entering the required information, click on the "Predict" button.
3. **View Prediction**: The application will display whether the customer is likely to churn or not based on the provided input.

