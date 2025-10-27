# BDAProject

Big Data Analytics Project: Vegetable Mandi Market Analysis using PySpark

OVERVIEW

This project analyzes the Indian Vegetable Mandi (wholesale market) dataset using Apache PySpark. The goal is to uncover insights into agricultural commodity pricing, market activity distribution, and regional variations across different states in India based on a single day's snapshot of data. The analysis employs PySpark DataFrames for large-scale data processing and aggregation, alongside Pandas and Matplotlib for data handling and visualization.

DATASET

Source: Government Mandi Data (mandi.csv) Description: Contains records of commodity arrivals and prices (Minimum, Maximum, Modal) from various Mandis across India. Key Features: State, District, Market, Commodity, Variety, Grade, Arrival_Date, Min_Price, Max_Price, Modal_Price. Size & Scope: 1,370 records covering 19 States, 121 Districts, 178 Markets, 119 Commodities, and 147 Varieties. Timestamp: All records correspond to a single date: 30/09/2025. Data Quality: The dataset used for analysis was clean, with no missing values detected in critical price or commodity columns.

OBJECTIVES

Analyze the geographic distribution of Mandi market activity across Indian states.
Identify states and commodities with the highest and lowest average prices.
Determine the most frequently traded commodities.
Assess price volatility/stability across different states using standard deviation.
Identify state-commodity combinations with the highest recorded prices.
Visualize key findings to provide clear insights into market dynamics.

TECHNOLOGIES USED
Big Data Processing: Apache Spark (v3.5.6) via PySpark
Programming Language: Python
Data Manipulation: Pandas
Data Visualization: Matplotlib
Environment: Jupyter Notebook

ANALYSIS HIGHLIGHTS & KEY FINDINGS
Data Loading & Preparation:
Loaded mandi.csv into a PySpark DataFrame, inferring schema.
Cleaned and converted the Arrival_Date column to a timestamp format.
Converted price columns to numeric types for calculations.

Geographic Distribution:
Kerala has the highest number of Mandi entries (279), while Andhra Pradesh and Bihar have the lowest (1 and 2, respectively).
Visualization: Bar chart showing states with the highest and lowest entry counts.

Average Price Analysis:
The overall average Modal Price across all states is approximately ₹3763.87.
Nagaland shows the highest average Modal Price (₹7305.88).
Bihar shows the lowest average Modal Price (₹2300.00).
Visualization: Bar charts highlighting the states with the highest and lowest average prices.

Commodity Analysis:
Top 5 Highest Average Price Commodities: Black pepper, Arecanut, Coconut Oil, Cummin Seed, Mustard Oil.
Bottom 5 Lowest Average Price Commodities: Identified through aggregation.
Most Frequent Commodity: Potato (listed 79 times).
Highest Commodity Diversity: Kerala (56 unique commodities).
Visualization: Bar charts for top/bottom commodities by price and most frequent commodity.

Price Volatility:
Calculated the standard deviation of Modal Prices per state.
Karnataka exhibits the highest price variation (Std Dev: ₹9756.14).
Thondekai appeared to be the most stable commodity price-wise, but this was due to having only one data point.
Visualization: Bar chart showing the top 10 states with the highest price standard deviation.

Highest Recorded Price:
Identified the top state-commodity combinations based on the highest recorded Modal Price.
Black pepper in Kerala recorded the single highest price (₹65,000).
Visualization: Bar chart displaying the top 10 highest individual price records.

CONCLUSION
The analysis provides valuable insights into the structure and pricing dynamics of Indian agricultural wholesale markets on the given date. It highlights significant regional disparities in activity, pricing, and stability. While the single-day snapshot limits trend analysis, the findings offer a strong foundation for understanding market characteristics and can inform decisions for farmers, traders, and policymakers. Expanding the dataset to include time-series data would enable more powerful predictive analytics.
