# Model Comparison

## Comparison of Simple and Multiple Regression Models

| Comparison Item       | Simple Regression Model (Footfall)                                                                                                     | Multiple Regression Model                                                                                                                                                                                                             |
| --------------------- | -------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Model Name            | Simple Linear Regression                                                                                                               | Multiple Linear Regression                                                                                                                                                                                                            |
| Dependent Variable    | monthly_sales                                                                                                                          | monthly_sales                                                                                                                                                                                                                         |
| Independent Variables | footfall                                                                                                                               | footfall, marketing_spend, customer_rating, Region_West, Region_North, Region_South                                                                                                                                                   |
| R-squared             | 0.7363                                                                                                                                 | 0.7924                                                                                                                                                                                                                                |
| Significant Variables | Footfall (p-value = 5.70E-96)                                                                                                          | Footfall (5.70E-96), Marketing Spend (1.07E-15), Region_West (0.0035), Region_South (0.0024)                                                                                                                                          |
| Business Usefulness   | Useful for understanding the effect of customer footfall on monthly sales. Simple to interpret but considers only one business factor. | Provides a more comprehensive explanation of monthly sales by combining customer traffic, marketing investment, and regional differences. Suitable for business decision-making and sales prediction.                                 |
| Limitations           | Ignores the influence of other business variables and may omit important factors affecting sales.                                      | Customer Rating and Region_North are not statistically significant. The model explains approximately 79.24% of the variation in monthly sales, indicating that additional factors not included in the model may also influence sales. |

---

## Overall Comparison

The multiple regression model performs better than the simple regression model because it explains a larger proportion of the variation in monthly sales. The R-squared value increased from 0.7363 in the simple regression model to 0.7924 in the multiple regression model, indicating improved explanatory power.

Footfall remains the most influential predictor in both models. Marketing Spend also contributes significantly to predicting monthly sales after accounting for the other variables. The West and South regions show significantly higher monthly sales than the reference region (East), demonstrating that geographical location also influences business performance.

Although Customer Rating and Region_North were included in the model, their p-values are greater than 0.05, indicating that they are not statistically significant predictors in the current model and should be interpreted with caution.

Overall, the multiple regression model provides better predictive performance and richer business insights than the simple regression model, making it the preferred model for explaining and predicting monthly sales.

