# Residual Analysis

## Task 7: Predictions and Residual Analysis

### 1. Objective

The objective of this analysis is to evaluate the performance of the multiple regression model by comparing the predicted monthly sales with the actual monthly sales. Residual analysis helps assess the accuracy of the model and identify observations where the prediction error is relatively high.

Note : The entire set of Residuals are generated inside Predictions_Residuals tab of regression_workbook. Only the analysis part is added here.
---

### 2. Prediction Method

Predicted monthly sales were generated using the final multiple regression model developed in Task 5.

The model included the following independent variables:

* footfall
* marketing_spend
* customer_rating
* Region_West
* Region_North
* Region_South

The dependent variable is:

* monthly_sales

---

### 3. Residual Calculation

Residuals were calculated using the following equation:

Residual = Actual Monthly Sales − Predicted Monthly Sales

A positive residual indicates that the actual monthly sales were higher than the predicted value, while a negative residual indicates that the model predicted higher sales than were actually observed.

---

### 4. Largest Prediction Errors

#### Top 5 Positive Residuals

| Observation | Predicted Sales |  Residual |
| ----------: | --------------: | --------: |
|         112 |       575269.59 | 138341.57 |
|         104 |       509046.62 | 116467.42 |
|         298 |       659155.01 | 104007.44 |
|           8 |       749477.97 | 100686.29 |
|         254 |       703537.96 |  95508.98 |

These observations represent cases where the regression model underestimated monthly sales.

---

#### Top 5 Negative Residuals

| Observation | Predicted Sales |   Residual |
| ----------: | --------------: | ---------: |
|          33 |       777496.08 | -135631.05 |
|          45 |       730038.96 | -134571.36 |
|          90 |       757130.29 | -129958.39 |
|          67 |       812350.01 | -126970.93 |
|         137 |       754119.92 | -120481.89 |

These observations represent cases where the regression model overestimated monthly sales.

---

### 5. Interpretation of Residuals

The residual analysis indicates that the regression model generally provides reliable predictions for monthly sales. Most observations have residual values close to zero, indicating good agreement between the predicted and actual values.

Some observations exhibit relatively large positive or negative residuals, indicating that the model was unable to fully capture the factors influencing monthly sales for those stores. These prediction errors may be due to business factors that are not included in the current regression model.

Overall, the distribution of positive and negative residuals suggests that the model does not consistently overestimate or underestimate monthly sales.

---

### 6. Discussion of Under-Prediction and Over-Prediction

The model exhibits both under-prediction and over-prediction across different observations.

The largest positive residual was 138341.57, indicating that the actual monthly sales exceeded the predicted sales by a substantial margin. Conversely, the largest negative residual was -135631.05, indicating that the predicted monthly sales were significantly higher than the actual sales.

Although a small number of observations show relatively large prediction errors, the overall model remains reliable. The multiple regression model explains approximately 79.24% of the variation in monthly sales (R-squared = 0.7924), indicating strong predictive performance. The presence of both positive and negative residuals suggests that the prediction errors are balanced rather than systematically biased toward over-prediction or under-prediction.

---

## Conclusion

The residual analysis demonstrates that the multiple regression model provides a good fit for the dataset. Most prediction errors are relatively small, while only a few observations show larger deviations between actual and predicted monthly sales. Overall, the model is suitable for explaining and predicting monthly sales and provides reliable insights for business decision-making.

