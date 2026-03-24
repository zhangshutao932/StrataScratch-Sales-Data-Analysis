📊 Sales Event Log Analysis — Time Series & Behavioral Insights
## 🧠 Project Overview

This project analyzes transactional sales event log data over a 50-week period to understand temporal sales dynamics, detect structural changes in demand, and explore behavioral patterns such as gender composition and time-of-day purchasing behavior.

The dataset originally consists of raw transaction-level logs. Through a sequence of analytical transformations, the data is reshaped into multiple representations suitable for:

Time-series analysis
Statistical hypothesis testing
Behavioral segmentation
Feature engineering

This project demonstrates core data science competencies in transforming raw event data into structured analytical datasets.

## 📁 Dataset Description

The raw dataset contains transaction-level records:

sale_time — timestamp of purchase
purchaser_gender — gender of customer

Each row represents a single purchase event.

This format is known as event log data, commonly used in real-world product analytics systems.

🔄 Data Transformation Pipeline

A key objective of this project is to illustrate how raw behavioral logs can be transformed into multiple analytical representations.

1️⃣ Event → Daily Time Series

Transactions were aggregated to compute daily sales volume:

Converted timestamps to calendar dates
Counted number of transactions per day

Resulting dataset:

Unit of analysis: day
Purpose: temporal trend analysis
2️⃣ Change Detection via Temporal Feature Engineering

To detect structural changes in demand:

Previous day sales were computed
Daily differences were calculated

This enabled identification of the largest discontinuity in the sales time series.

3️⃣ Statistical Significance Testing

The dataset was partitioned into:

Pre-change period
Post-change period

A Welch’s two-sample t-test was conducted to evaluate whether the shift in average daily sales was statistically significant.

This demonstrates construction of a statistical inference dataset from time-series data.

4️⃣ Behavioral Composition Analysis (Gender)

Sales were aggregated by:

Day
Purchaser gender

This produced a panel dataset capturing demographic composition over time.

A gender ratio feature was constructed to explore whether changes in demand were associated with shifts in customer demographics.

5️⃣ Temporal Behavioral Segmentation (Daypart)

Timestamps were discretized into behavioral categories:

Night (12am–6am)
Morning (6am–12pm)
Afternoon (12pm–6pm)
Evening (6pm–12am)

This enabled analysis of purchasing patterns across daily activity cycles.

## 🧮 Methods & Techniques Used
Data Engineering
Event log ingestion and concatenation
Timestamp parsing and transformation
Feature engineering (lag features, categorical binning)
Time Series Analysis
Daily aggregation
Structural change detection
Statistical Analysis
Welch’s t-test for mean comparison
Behavioral Analytics
Demographic aggregation
Ratio analysis
Temporal segmentation
Visualization
Time series plotting
Dual-axis behavioral trend visualization
🛠️ Technologies
Python
Pandas
NumPy
Matplotlib
SciPy
## 🎯 Learning Objectives

This project demonstrates:

Transforming raw event data into analytical datasets
Changing unit of analysis (transaction → day → demographic panel)
Constructing statistical test datasets
Behavioral feature engineering
Time-series reasoning
## 🚀 Future Improvements
Apply change-point detection algorithms
Build forecasting models (ARIMA / Prophet)
Conduct causal analysis of demand shift
Explore seasonality decomposition
Develop machine learning demand prediction
