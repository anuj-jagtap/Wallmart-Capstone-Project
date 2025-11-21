# Wallmart-Capstone-Project

📊 Walmart Weekly Sales Forecasting and Impact Analysis (SARIMA/SARIMAX)
This project, developed as a Capstone for my Data Science and AI coursework, focuses on solving a critical inventory management challenge for a major US retail chain using advanced time series analysis and statistical modeling.

Project Goal
The primary objective was twofold:
1.	Analyze the statistical impact of macro-economic and environmental factors (CPI, Unemployment, Temperature) on weekly store sales.
2.	Forecast weekly sales for strategic stores for the next 12 weeks to optimize supply chain and staffing decisions.

Technical Stack & Methods
•	Programming Language: Python
•	Core Libraries: Pandas, NumPy, Matplotlib, statsmodels (for Time Series)
•	Modeling Techniques:
o	Exploratory Data Analysis (EDA): Time series decomposition, outlier analysis, and stationarity testing (ADF test).
o	SARIMAX (Seasonal AutoRegressive Integrated Moving Average with eXogenous variables): Initially used to assess the statistical significance of external regressors.
o	SARIMA (Seasonal ARIMA): The final, stable predictive model, which successfully captures the dominant 52-week seasonality.

Key Business & Statistical Insights
The analysis directly addressed the client's inventory problem by quantifying sales drivers:

1. Dominance of Seasonality (Time Series Insight)
•	Finding: Weekly Sales exhibit high 52-week seasonality (annual cycle). 
•	Reason: Sales peak massively in the last quarter due to U.S. holidays, particularly Thanksgiving and Christmas.
•	Impact: Inventory and labor strategies must be optimized around these predictable spikes.

2. Insignificance of External Factors
•	Finding: External variables (Temperature, CPI, Unemployment, Fuel Price) were found to be statistically insignificant (P-value > 0.05) in predicting sales.
•	Conclusion: Walmart's weekly sales are highly inelastic to minor economic fluctuations. The simplified SARIMA model, excluding these variables, provides a more stable and efficient forecast.

3. Critical Performance Gap
•	Analysis: Aggregated total sales over the historical period (2010-2012) to rank all 45 stores.
•	Finding: A severe performance disparity exists: the Best Performing Store (20) sold 711% more than the Worst Performing Store (33).
•	Recommendation: Immediate operational investigation is required for low-performing stores to diagnose root causes.

📈 12-Week Sales Forecast
Using the highly robust $\mathbf{SARIMA(1, 1, 1) \times (1, 0, 0)_{52}}$ model, sales forecasts were generated for 5 strategically selected stores (Highest, High, Medium, Low, Worst). The forecast successfully predicts major revenue spikes in the weeks ending November 23rd (Black Friday) and December 21st (Christmas).

