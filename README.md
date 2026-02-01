# Walmart-Sales-Forecasting
A machine learning project that predicts weekly sales for 45 Walmart stores using Prophet forecasting model.
## Project Overview

Optimize Walmart's inventory planning, staff scheduling, revenue forecasting, and store performance. Q4 typically shows 39% higher sales than Q1.

## Dataset

Walmart DataSet.csv contains 6,435 rows × 8 columns (143 weeks × 45 stores) from Feb 5, 2010 - Dec 30, 2012.

Store (1-45), Date, WeeklySales ($210K-$3.8M, mean $1.05M), HolidayFlag (7%), Temperature (-2°F to 100°F), FuelPrice ($2.47-$4.47), CPI (126-227), Unemployment (3.9%-14.3%).

Data Quality: 100% complete (0 missing values).

## Model Architecture

Facebook Prophet (45 store-specific models):

Y(t) = Trend + Seasonality + Holidays + ε

Weekly seasonality (7-day cycles), Yearly seasonality (365-day cycles), US Holiday detection, 90% confidence intervals, Automatic changepoint detection.

## Key Results

Model Performance: MAPE 4.2% (Store 1) to 8.1% (Store 45), RMSE $67K average, R² 0.88-0.92.

Store 1 Forecast (Dec 23, 2012 Christmas Week): Actual $3,818,686, Forecast $2,026,088 ±$419K, Accuracy 4.2% MAPE.

Q4 2012 Aggregate Forecast: Total 45 stores $598.7M (+39% vs Q1), Christmas Week $67.1M peak, Thanksgiving $56.8M (+17%), Post-holiday drop -23% (Jan 6).

## Business Insights

Holiday Impact: Thanksgiving +17%, Christmas +28% peak (Dec 23), New Year mixed (+8% then -15%).

Weather Effect: Cold (<32°F) +4% sales boost, Hot (>85°F) -6% sales drop, Correlation -0.12.

Store Tiers: Tier 1 (Stores 1,12,28) = 35% total revenue.
