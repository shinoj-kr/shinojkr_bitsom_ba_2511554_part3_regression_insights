
# Task 3: Dummy Variable Approach

## Why Dummy Variables are Created

The dataset contains categorical variables such as region,store_type,and month. Since linear regression requires numerical input variables, categorical variables cannot be used directly in the regression model.

Dummy variables were therefore created to convert categorical values into binary (0/1) variables while preserving their categorical meaning.

---

## Region Dummy Variables

The region variable contains four categories:

- East
- West
- North
- South

To avoid the dummy variable trap (perfect multicollinearity), one category must be used as the reference category.

Reference Category: East

The following dummy variables are created:

- Region_West
- Region_North
- Region_South

Encoding:

| Region | Region_West | Region_North | Region_South |
|--------|------------:|-------------:|-------------:|
| East (Reference) | 0 | 0 | 0 |
| West | 1 | 0 | 0 |
| North | 0 | 1 | 0 |
| South | 0 | 0 | 1 |

---

## Store Type Dummy Variables

The store_type variable contains four categories:

- Residential
- Airport
- High Street
- Mall

Reference Category: Residential

The following dummy variables are created:

- Store_Airport
- Store_HighStreet
- Store_Mall

Encoding:

| Store Type | Store_Airport | Store_HighStreet | Store_Mall |
|------------|--------------:|-----------------:|-----------:|
| Residential (Reference) | 0 | 0 | 0 |
| Airport | 1 | 0 | 0 |
| High Street | 0 | 1 | 0 |
| Mall | 0 | 0 | 1 |

---

## Month Variable

The month column is retained in its original YYYY-MM format.

Although month is a categorical variable, dummy variables are not created because the assignment requires dummy variables for at least one categorical variable , and the selected regression model does not include month as an explanatory variable.

---

## Why One Category is Omitted

One category from each categorical variable is intentionally excluded and used as the reference category.

This prevents perfect multicollinearity (also known as the dummy variable trap) and allows the regression coefficients to be interpreted relative to the reference category.

- Region Reference Category: East
- Store Type Reference Category: Residential

The coefficients of the dummy variables therefore represent the expected difference compared with the corresponding reference category while holding all other variables constant.

# Model Equations

## Task 8: Regression Model Equations

### 1. Simple Regression Equations

#### Model 1: Marketing Spend

Regression Equation:

**Monthly Sales = 560777.35 + (2.1296 × Marketing Spend)**

Business Interpretation:

The model estimates that monthly sales increase by approximately **2.13 units** for every one-unit increase in marketing spend. Although the relationship is statistically significant, marketing spend alone explains only a small proportion of the variation in monthly sales.

---

#### Model 2: Footfall

Regression Equation:

**Monthly Sales = 446410.58 + (35.6780 × Footfall)**

Business Interpretation:

The model estimates that monthly sales increase by approximately **35.68 units** for every additional customer visiting the store. Among the simple regression models, Footfall is the strongest predictor of monthly sales.

---

### 2. Multiple Regression Equation

Regression Equation:

**Monthly Sales = 344215.49 + (33.8789 × Footfall) + (1.1690 × Marketing Spend) + (9065.43 × Customer Rating) + (20182.14 × Region_West) + (11935.97 × Region_North) + (23710.75 × Region_South)**

This equation estimates monthly sales by simultaneously considering customer traffic, marketing expenditure, customer rating, and regional differences.

---

### 3. Explanation of Each Coefficient

| Variable        | Business Interpretation                                                                                                                                                                                            |
| --------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Intercept       | Represents the estimated monthly sales when all numerical variables are zero and the store belongs to the reference region (East).                                                                                 |
| Footfall        | Each additional customer is associated with an increase of approximately **33.88** units in monthly sales, assuming all other variables remain constant.                                                           |
| Marketing Spend | Each additional unit of marketing spend is associated with an increase of approximately **1.17** units in monthly sales while holding the other variables constant.                                                |
| Customer Rating | A one-point increase in customer rating is associated with an estimated increase of approximately **9,065.43** units in monthly sales. However, this variable is not statistically significant in the final model. |
| Region_West     | Stores in the West region are expected to generate approximately **20,182** more monthly sales than stores in the East region.                                                                                     |
| Region_North    | Stores in the North region are expected to generate approximately **11,936** more monthly sales than stores in the East region. However, this difference is not statistically significant.                         |
| Region_South    | Stores in the South region are expected to generate approximately **23,711** more monthly sales than stores in the East region.                                                                                    |

---

### 4. Explanation of Dummy Variables

The categorical variable **Region** was converted into dummy variables before fitting the multiple regression model.

The following dummy variables were created:

* Region_West
* Region_North
* Region_South

Each dummy variable takes the value:

* **1** if the observation belongs to that region.
* **0** otherwise.

This approach enables the regression model to estimate the impact of each region on monthly sales while avoiding the dummy variable trap.

---

### 5. Reference Category Used

The **East** region was selected as the reference category.

For observations in the East region:

* Region_West = 0
* Region_North = 0
* Region_South = 0

The coefficients for the remaining regions represent the expected difference in monthly sales compared with stores located in the East region.

---

### 6. Final Model Selected

The **Multiple Linear Regression** model was selected as the final predictive model.

---

### 7. Reason for Selecting the Final Model

The multiple regression model was selected because it provides the highest explanatory power among all evaluated models. It explains approximately **79.24%** of the variation in monthly sales (R-squared = **0.7924**), which is higher than both simple regression models.

The model combines multiple business factors, including customer footfall, marketing expenditure, customer rating, and regional differences, providing a more comprehensive explanation of monthly sales. The adjusted R-squared value (**0.7885**) is close to the R-squared value, indicating that the additional variables improve the model while maintaining a good balance between model complexity and predictive performance.

Overall, the multiple regression model provides the most reliable insights for business decision-making and monthly sales prediction.

