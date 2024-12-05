# Predicting Restaurant Tips using Excel

This project aims to build a predictive model for restaurant tips using Microsoft Excel and the Data Analysis Add-in. The dataset contains various features of customer dining behavior, such as bill amount, customer demographics, and dining preferences. By using regression analysis, we develop a mathematical equation to predict tips and evaluate the model's performance.

## Dataset Description

The dataset, `Restaurant Tips Dataset.xlsx`, includes the following features:

- **sex**: Gender of the customer
- **smoker**: Indicates if the customer is a smoker or not
- **day**: Day of the restaurant visit
- **time**: Indicates whether the tip was for lunch or dinner
- **size**: Number of members dining
- **total_bill**: Bill amount in USD
- **tip**: Tip amount in USD (Target variable)

## Project Steps

### Step 1: Data Cleaning and Preprocessing

- Identified and filtered blank cells and duplicate rows in the dataset.
- Checked for missing values and cleaned the data.

### Step 2: Identifying Variables

- **Independent Variables**: `sex`, `smoker`, `day`, `time`, `size`, `total_bill`
- **Dependent Variable**: `tip`

### Step 3: Encoding Categorical Variables

- Converted categorical variables (`sex`, `smoker`, `day`, `time`) into numerical values using the `IFS` function in Excel.

### Step 4: Correlation Analysis

- Calculated correlation coefficients between the numerical variables to identify their relationships.

### Step 5: Regression Model Building

- Performed regression analysis with all independent variables:
  - Observed that the **p-values** of `sex`, `smoker`, `day`, and `time` were greater than 0.05, indicating low statistical significance.
- Refined the model by using only the significant variables: `size` and `total_bill`.

### Step 6: Prediction Formula

- Derived the following predictive formula for calculating tips:

```Predicted Tip = Intercept + (Coefficient for Size × Size) + (Coefficient for Total Bill × Total Bill)```

- Calculated predicted tips for all observations in the dataset.

### Step 7: Model Evaluation

- Evaluated the model using Root Mean Square Error (RMSE):
- **Squared Error**: `(Actual Tip - Predicted Tip)^2`
- **Mean of Squared Errors**: Average of squared error values.
- **RMSE**: Square root of the mean squared errors.

## Results

- Developed a regression model to predict restaurant tips based on significant predictors: `size` and `total_bill`.
- Calculated predicted tips and compared them to actual tips to evaluate the model's accuracy.
- Computed RMSE as a measure of model performance.

## Tools Used

- **Microsoft Excel**
- **Data Analysis Add-in**

## Deliverables

1. Predictive model for restaurant tips.
2. Mathematical formula for predicting tips:
```Predicted Tip = Intercept + (Coefficient for Size × Size) + (Coefficient for Total Bill × Total Bill)```
3. RMSE as a performance metric.

## How to Use This Project

1. Open the `Restaurant Tips Dataset.xlsx` file in Excel.
2. Follow the steps outlined above to preprocess the data and build the model.
3. Use the regression analysis output to predict tips for new observations.
4. Evaluate model performance with RMSE.

## Conclusion

This project demonstrates how to use Microsoft Excel for predictive analytics by building a model to predict restaurant tips based on customer dining behavior. The model highlights the importance of significant predictors like bill amount and group size in determining tip amounts.
