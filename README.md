# Intro-To-Data-Science-Final-Project
IDC 3140: Applied Data Analytics | Florida Gulf Coast University
📌 Project Overview

This project demonstrates a complete data analysis pipeline designed to predict the next-day price movement (Up/Down) of NVIDIA (NVDA) stock. Utilizing historical data from 1999 to 2024, the system ingests raw, unstandardized CSV data, performs advanced feature engineering, and utilizes a Random Forest Classifier to generate predictive insights.
🎯 Objectives

    Data Sanitization: Automate the cleaning of raw financial datasets containing non-numeric characters (currency symbols, commas).

    Statistical Analysis: Implement institutional-grade indicators such as Bollinger Bands, RSI, and Moving Averages.

    Structured Querying: Utilize SQL (pandasql) to extract seasonal trends and market "shock" events.

    Interactive Interface: Provide a robust, terminal-based system for live inference and system status updates.

🛠️ Technical Implementation

This repository contains over 400 lines of Python code focusing on the following core software engineering principles:

    Modularization: Logic is encapsulated within functions (e.g., predict_tomorrow(), main_menu()) for reusability.

    Exception Handling: Robust try...except blocks manage invalid user inputs in the interactive terminal.

    Data Structures: Advanced use of Pandas DataFrames, NumPy arrays, and SQL-style relational tables.

    Control Loops: A persistent main menu loop allows for a continuous user experience.

📊 Data Pipeline & Methodology

    Preprocessing: Raw string-based currency data is cleaned using Regular Expressions (Regex) and converted to float64 types.

    Feature Engineering: * Trend: 10-day and 50-day Simple Moving Averages (SMA).

        Momentum: Relative Strength Index (RSI).

        Volatility: Bollinger Bands (Standard Deviation envelopes).

    Exploratory Data Analysis (EDA): Visualized through Matplotlib and Seaborn to identify "Fat Tail" distributions and price-momentum correlations.

    SQL Analysis: Seasonal performance metrics were queried using SQL strftime and GROUP BY operations.

🚀 How to Run the Project

    Clone the repository:
    Bash

    git clone https://github.com/[Your-Username]/[Your-Repo-Name].git

    Install the required dependencies:
    Bash

    pip install pandas numpy matplotlib seaborn scikit-learn pandasql

    Open the Jupyter Notebook or run the script:

        Ensure nvda_stock_data_raw_nasdaq.csv is in the same directory.

        Execute all cells.

        Interact with the Live Prediction System in the final cell.

📈 Results & Discussion

    Model Performance: The Random Forest Classifier achieved a baseline accuracy of approximately 50%. While stock markets are highly efficient, the model successfully identifies periods of extreme overbought/oversold conditions using RSI and Bollinger Bands.

    Feature Importance: Trend indicators (SMAs) and Volatility were identified as the strongest predictors for next-day movement.

⚠️ Limitations & Future Work

    Sentiment Analysis: Current predictions are based solely on technical price action. Integrating news sentiment or earnings call transcripts would be a logical next step.

    Hyperparameter Tuning: Future iterations could utilize GridSearchCV to optimize the Random Forest depth and estimator count.

📚 References

    Pedregosa, F., et al. (2011). Scikit-learn: Machine Learning in Python. Journal of Machine Learning Research.

    Hayes, A. (2024). Simple Moving Average (SMA): What It Is and How It's Calculated. Investopedia.

    Pandas Development Team. (2024). User Guide: Working with Text Data (Regular Expressions).
