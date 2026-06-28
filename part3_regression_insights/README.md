# Business Problem

A retail chain wants to understand which business factors have the greatest impact on monthly store sales. Leadership plans to use these insights to make better decisions regarding marketing investment, staffing, inventory management, pricing strategy, and store operations.

The goal of this project is to identify the variables that are most strongly associated with monthly sales using regression analysis and provide business recommendations based on the results.

---

# Dataset Description

The dataset contains monthly business information for multiple retail stores.

It includes store characteristics, marketing activity, customer behaviour, operational measures, and financial performance.

The target variable is monthly sales, while the remaining variables are potential predictors that may help explain differences in sales across stores.

---

# Dependent Variable

The dependent variable is:

* Monthly Sales (`monthly_sales`)

This is the variable we want to predict.

---

# Independent Variables

Potential independent variables include:

* Marketing Spend
* Footfall
* Average Discount Percentage
* Staff Count
* Inventory Availability Percentage
* Competitor Distance
* Holiday Flag
* Customer Rating
* Region
* Store Type

These variables may influence monthly sales and will be tested using regression analysis.

---

# Numerical Variables

The numerical variables include:

* Marketing Spend

* Footfall

* Average Discount Percentage

* Staff Count

* Inventory Availability Percentage

* Competitor Distance

* Customer Rating

* Monthly Sales

* Monthly Profit

---

# Categorical Variables

The categorical variables include:

* Region
* Store Type
* Month
* Holiday Flag

---

# Variables That May Need Cleaning or Transformation

The following checks should be performed before regression analysis:

* Missing values

* Duplicate records

* Incorrect data types

* Outliers in numerical variables

* Dummy variable creation for Region and Store Type

---

# Variables That May Not Be Useful for Regression

The following variables are unlikely to be used directly in the regression model:

* Store ID (acts only as a unique identifier)

* Monthly Profit (this is another business outcome rather than a predictor of sales)


These variables will not be included as predictors in the final regression model.

---

---

# Regression Approach

The regression analysis was performed using Microsoft Excel's Data Analysis ToolPak.

The following models were created:

* Simple Regression Model 1: Marketing Spend vs Monthly Sales
* Simple Regression Model 2: Footfall vs Monthly Sales
* Multiple Regression Model: Marketing Spend, Footfall, Inventory Availability, and Airport Dummy vs Monthly Sales

The regression outputs were used to evaluate coefficients, R² values, p-values, and the business importance of each variable.

---

# Dummy Variable Approach

The categorical variable **Store Type** was converted into dummy variables before running the multiple regression model.

The following dummy variables were created:

* Airport Dummy
* High Street Dummy
* Mall Dummy

Residential was selected as the reference category and was therefore excluded from the regression model to avoid perfect multicollinearity (the dummy variable trap).

The final regression model used the Airport Dummy variable.

---

# Model Comparison Summary

Three regression models were compared.

| Model                               | R²    | Summary                                               |
| ----------------------------------- | ----- | ----------------------------------------------------- |
| Simple Regression (Marketing Spend) | 0.167 | Moderate predictor of monthly sales                   |
| Simple Regression (Footfall)        | 0.736 | Strong predictor of monthly sales                     |
| Multiple Regression                 | 0.809 | Best overall model with the highest explanatory power |

The multiple regression model explained approximately 80.9% of the variation in monthly sales and was selected as the final model.

---

# Final Model Selected

The Multiple Regression Model was selected because it achieved the highest R² value (0.809) and included multiple important business drivers.

The model provides the strongest explanation of monthly sales and is the most suitable for supporting business decisions.

---

# Business Recommendation

The analysis suggests that leadership should focus on increasing customer footfall, maintaining high inventory availability, and investing marketing budgets effectively to improve monthly sales.

Airport stores also showed higher expected sales compared with the reference category, indicating that store type may influence performance.

The regression model should be used as a decision-support tool together with business knowledge and operational experience.

---

# Assumptions and Limitations

* Regression analysis identifies associations but does not prove causation.
* Other business factors such as seasonality, local competition, pricing strategies, and economic conditions were not included in the dataset.
* The analysis assumes linear relationships between the selected variables and monthly sales.

---

# Screenshots Included

The repository includes the following screenshots:

* simple_regression_output.png
* multiple_regression_output.png
* residuals_preview.png
* model_comparison_preview.png

These screenshots provide evidence of the regression analysis and model comparison performed in this project.