# AshareQuant
Stock Trading Analysis and Strategy Framework

This repository provides a robust framework for analyzing stock trading data and implementing trading strategies using Python. It utilizes the Pandas and NumPy libraries to facilitate data manipulation, analysis, and decision-making based on historical stock data.

Key Features:
1. Data Import and Preprocessing:

2. Import stock market data using the efinance library.
Clean and preprocess data, including handling missing values and converting data types for accurate analysis.
Logarithmic Growth Calculations:

3. Calculate logarithmic growth for stock closing prices and trading volumes using the get_log_growth and get_volume_change functions.
These metrics help assess performance trends over time.
Data Filtering:

4. Filter stock data based on specific dates and business days using functions like get_filtered_df and get_filtered_df_after.
Retrieve today's stock data with the get_today function.
Growth and Volume Analysis:

5. Functions to compute total growth over specified periods for both prices and volumes (get_growth, get_vol_growth).
Calculate average trading volume with get_average_vol.
Trading Conditions Evaluation:

6. Assess various trading conditions, such as price increases over recent days, volume changes, and turnover rates.
Functions include whether_price_rise_in_last_n_days, whether_trade_vol_rise_in_last_n_days, and whether_turnover_rate_larger_than.
Portfolio Return Calculation:

7. Evaluate potential returns on investments with the get_portfolio_return function, which calculates the return based on selected stocks over a defined period.
Strategy Implementation:

8. The framework allows users to define and implement trading strategies based on specific criteria, such as price thresholds and volume conditions.
The strategy is executed over a range of working days, filtering stocks that meet predefined conditions.


Output and Reporting:

Results are compiled into a DataFrame, which can be exported to Excel for further analysis or reporting.
The repository includes functionality to track execution time for performance optimization.

Usage Instructions:
1. Setup: Ensure you have the required libraries installed: pandas, numpy, efinance, and any other dependencies.
2. Data Loading: Load stock data using the provided functions. Ensure that the data is cleaned and preprocessed to fit the expected format.
3. Define Strategy Parameters: Set your trading strategy parameters, such as thresholds for price changes and volume conditions.
4. Run Analysis: Execute the analysis by running the main script. The script will filter stocks based on the defined
strategy and output the results.


Review Results:

Check the generated Excel file for selected stocks, their performance metrics, and any other relevant information.

StockScreen3:
This repository contains a backtesting framework designed for stock trading strategies, focusing on analyzing stock performance over a specified period. The backtest runs from December 1, 2022, to November 21, 2023, allowing users to evaluate the effectiveness of various trading tactics based on historical data.

Key Features:
Date Configuration: Users can set the start and end dates for the backtest.
Working Days Calculation: Generates a list of working days while excluding national holidays.
Trading Strategy Parameters: Users can customize parameters such as volume thresholds, price changes, and turnover rates to refine their strategy.
Data Analysis: The framework analyzes stock performance metrics, including daily and multi-day growth percentages.
Results Compilation: The results are compiled into a DataFrame and exported to Excel for further analysis, including average returns and selected stock codes.
Usage:
1. Adjust the start_tactic_date and end_tactic_date variables to set your desired testing period.
2. Modify the trading strategy parameters as needed to fit your investment approach.
3. Run the script to execute the backtest and generate performance reports.
This repository is ideal for quantitative analysts and traders looking to backtest and optimize their stock trading strategies using historical data.
