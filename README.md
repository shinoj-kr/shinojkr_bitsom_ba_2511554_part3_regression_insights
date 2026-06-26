# Retail Store Sales Regression Analysis

## Business Problem Summary

This project analyzes monthly retail store performance to identify the key business factors associated with monthly sales using regression analysis. The objective is to develop predictive models that help management understand which operational, marketing, and regional factors have the greatest influence on sales and provide data-driven business recommendations.

---

## Dataset Description

The dataset contains monthly operational and business performance data for multiple retail stores. It includes information related to sales, marketing expenditure, customer behaviour, staffing, inventory availability, customer satisfaction, regional information, and profitability.

The dataset contains both numerical and categorical variables that were prepared for regression analysis through data cleaning and transformation.

---

## Dependent and Independent Variables

### Dependent Variable

* monthly_sales

### Independent Variables

Numerical Variables

* marketing_spend
* footfall
* avg_discount_pct
* staff_count
* inventory_availability_pct
* competitor_distance_km
* holiday_flag
* customer_rating
* monthly_profit

Categorical Variables

* region
* store_type
* month

---

## Regression Approach

Two simple linear regression models and one multiple linear regression model were developed.

Simple Regression Models

* Marketing Spend → Monthly Sales
* Footfall → Monthly Sales

Multiple Regression Model

Dependent Variable

* monthly_sales

Independent Variables

* footfall
* marketing_spend
* customer_rating
* Region_West
* Region_North
* Region_South

The multiple regression model was selected as the final predictive model because it provided the highest explanatory power.

---

## Dummy Variable Approach

Categorical variables were converted into dummy variables before building the multiple regression model.

Dummy variables created:

Region

* Region_West
* Region_North
* Region_South

Reference Category

* East

Store Type

* Airport
* High Street
* Mall

Reference Category

* Residential

The Month variable was not included in the final regression model because it was not required for the selected model.

---

## Model Comparison Summary

Three regression models were evaluated.

| Model                               | R-squared | Adjusted R-squared | Summary                        |
| ----------------------------------- | --------: | -----------------: | ------------------------------ |
| Simple Regression (Marketing Spend) |    0.1672 |             0.1646 | Weak explanatory power         |
| Simple Regression (Footfall)        |    0.7363 |             0.7355 | Strong simple regression model |
| Multiple Regression                 |    0.7924 |             0.7885 | Best performing model          |

The multiple regression model demonstrated the highest explanatory power and was therefore selected as the final predictive model.

---

## Final Model Selected

Multiple Linear Regression

R-squared: 0.7924

Adjusted R-squared: 0.7885

Significant Variables

* Footfall
* Marketing Spend
* Region_West
* Region_South

Variables requiring cautious interpretation

* Customer Rating
* Region_North

---

## Business Recommendation

The analysis identified Footfall as the strongest predictor of monthly sales, followed by Marketing Spend. Stores located in the West and South regions also demonstrated significantly higher sales than those in the reference region (East).

Management should prioritize initiatives that increase customer footfall, continue investing in effective marketing campaigns, and evaluate successful operational practices from high-performing regions. The regression model should be used as a decision-support tool while continuing to collect additional business data to improve future predictive models.

---

## Assumptions and Limitations

* Linear relationships between predictors and monthly sales were assumed.
* Regression identifies association and does not establish causation.
* The model explains approximately 79.24% of the variation in monthly sales.
* Approximately 20.76% of the variation may be explained by factors not included in the dataset.
* Customer Rating and Region_North were not statistically significant and should be interpreted cautiously.
* Residual analysis identified observations with larger prediction errors, suggesting opportunities to improve the model with additional explanatory variables.

---

## Screenshots Included

The following screenshots are included in the project:

* simple_regression_output.png
* multiple_regression_output.png
* residuals_preview.png
* model_comparison_preview.png

---

## Project Structure

```text
part3_regression_insights/
│
├── data/
│   └── business_regression_data.xlsx
│
├── analysis/
│   ├── regression_workbook.xlsx
│   ├── model_comparison.md
│   └── residual_analysis.md
│
├── outputs/
│   ├── regression_summary.xlsx
│   ├── model_equations.md
│   └── final_recommendation.md
│
├── screenshots/
│   ├── simple_regression_output.png
│   ├── multiple_regression_output.png
│   ├── residuals_preview.png
│   └── model_comparison_preview.png
│
└── README.md
```
