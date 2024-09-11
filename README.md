
# README

## Summary of Findings and Link to Notebook

This project involves exploring a dataset of 426,000 used cars, obtained from Kaggle, to determine the key factors that influence car pricing. The analysis aims to assist a used car dealership in optimizing their pricing strategy by identifying what consumers value most in a used car. Several machine learning models, including Linear Regression, Ridge Regression, and Lasso Regression, were applied to predict car prices based on various features.


---

## Business Understanding

The goal of this analysis is to optimize the pricing strategy for a used car dealership by identifying the most important factors influencing the price of used cars. This understanding will allow the dealership to make informed decisions about pricing, improve their inventory management, and maximize profitability while staying competitive in the market.

### Key Business Objectives:

1. Identify the most important variables that influence used car prices, such as age, mileage, condition, and brand.
2. Develop a reliable pricing model using regression techniques.
3. Provide actionable recommendations for pricing based on consumer demand and car attributes.

---

## Data Understanding and Preparation

The dataset included several key features like vehicle price, year, odometer reading, condition, manufacturer, fuel type, and more. 

### Key Steps:
- **Descriptive Statistics**: Numerical summaries were calculated to understand central tendencies, outliers, and variability in data.
- **Outlier Detection**: Boxplots were created for key variables like price and odometer to detect outliers.
- **Correlation Heatmap**: This was used to analyze relationships between variables such as price, year, and odometer.
- **Data Cleaning**: Missing values were identified and removed, and categorical variables were transformed using one-hot encoding. Outliers were removed using the Interquartile Range (IQR) method.

### Cleaned Data Summary:
- Rows after cleaning: 31,765
- Features used: year, condition, mileage, manufacturer, fuel, drive, size, type, cylinders, etc.

---

## Modeling Approach

Several regression models were applied to predict the price of a car based on the identified features:

1. **Linear Regression**: Provides a simple model to explain the relationship between car features and price.
2. **Ridge Regression**: Helps reduce overfitting by penalizing large coefficients.
3. **Lasso Regression**: Similar to Ridge, but also performs feature selection by shrinking some coefficients to zero.

### Model Evaluation:
- **R-squared**: Around 0.63 for all models, indicating that approximately 63% of the variance in car prices can be explained by the model.
- **Mean Squared Error**: Similar across the three models, indicating a comparable level of performance.
- **Feature Importance**: Vehicle age and odometer are the most important variables affecting the price. Other significant variables include condition and brand.

### Best Performing Model: Lasso Regression with an alpha value of 0.1

---

## Findings and Recommendations

### Key Insights:
1. **Vehicle Age**: Older cars generally have lower prices, but the decrease in price becomes more gradual after 10 years.
2. **Mileage**: Cars with lower mileage tend to command higher prices.
3. **Condition**: Cars in excellent or like-new condition significantly increase in price.
4. **Manufacturer**: Premium brands like BMW and Mercedes-Benz tend to hold their value better than budget brands.

### Actionable Recommendations:
- **Pricing Strategy**: Prioritize pricing based on mileage and vehicle age, as they are the key drivers of price. Cars with low mileage and excellent condition should be priced higher.
- **Inventory Decisions**: Focus on acquiring cars in good condition with fewer miles, as these features lead to higher resale value.
- **Brand-Specific Pricing**: Premium brand cars should be priced more competitively as they retain more value over time compared to economy brands.

---

## Next Steps and Recommendations

1. **Feature Engineering**: Additional features like geographical location, seasonality, and consumer demand trends could be incorporated for future analysis.
2. **Model Tuning**: While the current models perform well, experimenting with other algorithms (e.g., Random Forest, Gradient Boosting) could provide further improvements.
3. **Dynamic Pricing**: Implementing a dynamic pricing strategy that adjusts prices based on real-time data (e.g., market conditions) would enhance the dealership's ability to remain competitive.
4. **Data Collection**: Continuously improve data collection practices, especially around missing values and incorrect data entry, to ensure higher model accuracy.
