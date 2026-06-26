# Final Recommendation

## Task 9: Business Recommendations Based on Regression Analysis

### 1. Which factors appear most strongly associated with monthly sales?

The regression analysis indicates that **Footfall** is the strongest factor associated with monthly sales. It consistently demonstrated the highest explanatory power across both the simple and multiple regression models and remained highly statistically significant (p-value = 5.70E-96).

**Marketing Spend** also showed a positive and statistically significant relationship with monthly sales (p-value = 1.07E-15), indicating that increased marketing investment contributes to higher sales.

The regional dummy variables **Region_West** and **Region_South** were also statistically significant, suggesting that stores located in these regions generally achieve higher monthly sales than stores in the reference region (East).

---

### 2. Which variables should leadership focus on?

Based on the regression results, leadership should prioritize the following business factors:

* Increasing customer footfall through customer acquisition and retention initiatives.
* Investing in effective marketing campaigns to support sales growth.
* Studying the operational practices of stores in the West and South regions to identify strategies that can be implemented in other regions.
* Monitoring customer satisfaction as an important business metric, even though it was not statistically significant in the current regression model.

These factors provide the greatest opportunity to improve monthly sales according to the regression analysis.

---

### 3. Which variables should not be over-interpreted?

The regression analysis indicates that **Customer Rating** and **Region_North** should not be over-interpreted.

Although both variables have positive regression coefficients, their p-values are greater than 0.05, indicating that there is insufficient statistical evidence to conclude that they significantly influence monthly sales in the current model.

Management should therefore avoid making major business decisions based solely on these variables without additional supporting evidence.

---

### 4. What business action would you recommend?

Based on the regression findings, the following business actions are recommended:

* Increase initiatives that drive customer footfall, as it is the strongest predictor of monthly sales.
* Continue investing in marketing activities that demonstrate measurable returns.
* Evaluate the successful business practices of stores in the West and South regions and consider implementing similar strategies in other regions.
* Continue collecting additional operational and customer data to improve future predictive models and support more informed business decisions.

---

### 5. What risks or limitations should leadership keep in mind?

Although the multiple regression model performs well, several limitations should be considered:

* The model explains approximately **79.24%** of the variation in monthly sales, indicating that other factors not included in the dataset may also influence sales.
* Regression analysis identifies statistical relationships but cannot capture every business condition affecting store performance.
* Some variables, such as Customer Rating and Region_North, were not statistically significant and should therefore be interpreted cautiously.
* Prediction errors observed in the residual analysis indicate that certain stores may be affected by additional business factors not represented in the current model.

Leadership should use the regression model as one component of decision-making rather than as the sole basis for business decisions.

---

### 6. Why does regression show association but not automatically prove causation?

Regression analysis measures the strength and direction of relationships between variables, but it does not establish that one variable directly causes changes in another.

For example, while higher footfall is strongly associated with higher monthly sales, the regression model alone cannot prove that increasing footfall will always cause sales to increase. Other factors, such as promotions, product assortment, pricing strategies, local market conditions, and economic influences, may also contribute to sales performance.

Therefore, regression results should be interpreted as evidence of association rather than proof of cause-and-effect relationships.

---

## Final Recommendation

The multiple regression model is recommended as the final predictive model because it provides the highest explanatory power (R-squared = 0.7924) while incorporating multiple business factors. The analysis demonstrates that customer footfall, marketing spend, and regional differences are the most important drivers of monthly sales. Leadership should prioritize initiatives that increase customer traffic, optimize marketing investments, and leverage successful regional business practices, while continuing to evaluate additional business factors that may further improve sales prediction and decision-making.

