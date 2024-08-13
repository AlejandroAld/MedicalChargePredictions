# Medical Charge Predictions

This repository contains a project focused on predicting medical charges using machine learning techniques. The dataset used for this project is sourced from Kaggle and can be found [here](https://www.kaggle.com/datasets/mirichoi0218/insurance?resource=download).

## Project Overview

The goal of this project is to predict medical charges based on various factors such as age, BMI, smoking status, and more. We employ a Random Forest model to make these predictions and evaluate its performance. Additionally, we compare the results with a linear regression model to understand how well the Random Forest model captures the complexities of the data.

## Dataset

The dataset includes the following columns:

- **age**: Age of the primary beneficiary.
- **sex**: Gender of the beneficiary.
- **bmi**: Body mass index, a measure of body fat based on height and weight.
- **children**: Number of children covered by health insurance.
- **smoker**: Smoking status of the beneficiary.
- **region**: The beneficiary's residential area in the US.
- **charges**: Medical charges billed by health insurance.

## Key Observations

1. **Age and Charges**: Older individuals tend to have higher medical charges. The data suggests possible segmentation into three charge categories based on age.
2. **Children and Charges**: As the number of children increases, medical charges tend to decrease.

## Methodology

1. **Exploratory Data Analysis**:
   - Plots were generated to visualize the relationships between numeric variables such as age, BMI, and charges.
   - Correlation analysis was performed to understand the strength of relationships between variables.

2. **Model Training**:
   - A linear regression model was initially fitted to understand baseline relationships.
   - A Random Forest model was then trained using 10-fold cross-validation to predict medical charges. The model's hyperparameters were tuned to optimize performance.

3. **Model Evaluation**:
   - The Root Mean Square Error (RMSE) and R-squared values were calculated to assess the accuracy of the predictions.
   - The importance of each predictor was evaluated to understand the contribution of each feature to the model.

4. **Visualization**:
   - Predictions from the Random Forest model were plotted against observed charges.
   - A trend line from a linear regression model was added for comparison.

## Results

- The Random Forest model achieved an RMSE of approximately 2492.91.
- Smoking status was identified as the most significant predictor, followed by BMI and age.
- The model's predictions were visualized alongside a linear regression trend line to illustrate how well the Random Forest captures the data's complexity.

## Installation

To run this project locally, ensure you have R installed along with the following packages:

```r
install.packages("ggplot2")
install.packages("randomForest")
install.packages("caret")
