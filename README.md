# Predicting Gold Content in Gold Ore Using Machine Learning

## Introduction

This project aims to develop a machine learning model to predict the gold content in gold ore samples. By employing advanced data analysis techniques and machine learning algorithms, the project seeks to enhance the accuracy of gold content predictions, which is crucial for optimizing mining processes and resource management.

## Goal

The primary objective is to identify the most effective machine learning model for predicting gold content in gold ore. This involves selecting and evaluating models based on their performance and accuracy in forecasting gold content from the available data.

## Project Stages

1. **Data Loading and Preparation**
   - **Data Acquisition**: Load the datasets.
   - **Initial Analysis**: Examine the data characteristics.
   - **Error Calculation**: Compute the Mean Absolute Error (MAE).
   - **Data Cleaning**: Address missing columns and anomalies.

2. **Exploratory Data Analysis (EDA)**
   - **Feature Analysis**: Investigate changes in Au, Ag, and Pb concentrations.
   - **Distribution Study**: Analyze feature distributions in training and test datasets.
   - **Abnormality Detection**: Identify and handle anomalies.

3. **Model Development**
   - **sMAPE Calculation**: Develop a function to calculate symmetric Mean Absolute Percentage Error (sMAPE).
   - **Model Training**: Train various machine learning models and evaluate them using cross-validation.
   - **Model Evaluation**: Select and test the best model using the test dataset.

## Dataset Description

The datasets for this project are provided in three files:

- `gold_recovery_train.csv`: Training data
- `gold_recovery_test.csv`: Test data
- `gold_recovery_full.csv`: Complete dataset with all features

These files are indexed by date and time of acquisition. Some features might be missing in the test set due to timing differences in measurements. The source dataset provides a comprehensive view of all features.

## Conclusion

The project aims to understand which machine learning model best predicts the gold content within gold ore. Key findings and treatments include:

- **Dataset Details**:
  - Training Dataset: 16,860 rows, 87 columns
  - Test Dataset: 5,856 rows, 53 columns
  - Source Dataset: 22,716 rows, 87 columns

- **Missing Values**: Detected and filled with the mean value for each column.
- **Duplicate Values**: None found.
- **Mean Absolute Error (MAE)**: 81.79
- **Column Differences**: Resolved by aligning columns in both train and test datasets.
- **Data Splitting**: Train dataset split into training (75%) and validation (25%) sets.

- **Exploratory Data Analysis**:
  - **Concentration Trends**:
    - Au and Pb concentrations increase through the processing stages.
    - Ag concentration decreases through the stages.
  - **Distribution Observations**:
    - Input flotation process: Normal distribution between 6-8 points.
    - Output at various stages shows distributions mostly normal with some values of no gold.

- **Model Performance**:
  - **Linear Regression**: 10% sMAPE for both train and test datasets.
  - **Decision Tree Regressor**: 7% sMAPE for train dataset, 9% for test dataset.
  - **Random Forest Regressor**: 6% sMAPE for train dataset, 8% for test dataset.

- **Cross-Validation Results** (cv=10):
  - Linear Regression: 25.39%
  - Decision Tree Regressor: 16.06%
  - Random Forest Regressor: 39.88%

**Recommendation**: The Decision Tree Regressor is recommended due to its relatively low sMAPE scores (7% for train and 9% for test datasets) and cross-validation result (16.06%).
