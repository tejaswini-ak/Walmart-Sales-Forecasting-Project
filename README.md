# Walmart Sales Forecasting Project
This project focuses on forecasting sales for Walmart stores using time series models to help manage inventory and match supply with demand effectively.

### Problem Statement
Walmart is facing issues in managing inventory across its multiple outlets. The objective is to forecast sales accurately to ensure optimal inventory levels.
### Project Objective
1. Analyze the impact of various factors on weekly sales, including unemployment, fuel price, temperature, and Consumer Price Index (CPI).
2. Identify the best and worst-performing stores based on historical data.
3. Determine the best predictive modeling techniques to forecast sales for each store over the next 12 weeks.
### Data Description
* Number of Rows: 6435
* Number of Columns: 8
* Key Features:
   - Store: Numeric identifier for each store (int64)
   - Date: Date of the week of sales (object)
   - Weekly Sales: Sales for the given store in that week (float64)
   - Holiday Flag: Indicator for a holiday week (int64)
   - Temperature: Temperature on the day of the sale (float64)
   - Fuel Price: Cost of fuel in the region (float64)
   - CPI: Consumer Price Index (float64)
   - Unemployment: Unemployment Rate (float64)
### Data Pre-processing
1. Checked and handled missing values.
2. Extracted year, month, week, and day from the date column for more insights.
3. Handled outliers using the interquartile range technique.
4. Summarized the data for a better understanding.
### Data Insights
* Store 4 was the top performer, while store 33 had the least sales.
* Significant sales dates included 9th September 2011 and 23rd December 2011.
* Unemployment rates peaked in 2010, affecting store 38444 the most.
* CPI had a notable impact on store 361435.
* Sales showed a seasonal pattern with stability in the first quarter, a dip after June, and a rise in the last quarter.
### Algorithm Selection
Time series models such as ARIMA, SARIMA, and Facebook Prophet were considered. SARIMA was chosen for its ability to capture both seasonal and non-seasonal patterns effectively.

### Motivation for Choosing SARIMA
* The data exhibited complex seasonality and irregularities that ARIMA couldn't handle well.
* SARIMA performed better than Facebook Prophet, as indicated by a lower RMSE value (SARIMA: 69038.896 vs. Prophet: 98612.661).
### Assumptions
* Data is stationary, with consistent mean and variance over time.
* The chosen model order (p, d, q) and seasonal order (P, Q) are appropriate.
* The model is stable over time.
### Model Evaluation
* Evaluation Metric: RMSE
* SARIMA RMSE: 69038.896
* Facebook Prophet RMSE: 98612.661
### Inferences
* SARIMAX captured the seasonal and trend components effectively.
* Some differences between actual and predicted data may be due to outliers not fully captured by the model.
* Overall, SARIMAX is a good fit for the data.
### Future Possibilities
1. Personalized sales prediction for individual products or brands.
2. Incorporate external factors such as weather, holidays, and events into the model.
3. Explore other time series models, ensemble methods, or deep learning models for better accuracy.
### Conclusion
Data cleaning and preprocessing were essential for improving the accuracy of time series models. SARIMA was the best performing model, providing valuable insights for managing Walmart's inventory effectively.

### References
* Facebook. (2017). Prophet: Forecasting at scale. Available at: Prophet: Forecasting at scale
* Dataset: Kaggle
