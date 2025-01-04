# Pairs Trading with Kalman Filter

This project explores pairs trading using a dynamic, real-time hedge adjustment technique via the Kalman Filter. This project aims to help understand and implement pairs trading, an essential quantitative trading strategy, using Bayesian online training. This project is mentored by Nimay Shah and Devavrat Patni.

## Table of Contents
1. [Introduction](#1-introduction)
2. [Background](#2-background)
3. [Project Objectives](#3-project-objectives)
4. [Implementation Overview](#4-implementation-overview)
5. [Requirements](#5-requirements)
6. [Getting Started](#6-getting-started)
7. [Code and Explanation](#7-code-and-explanation)
8. [Conclusion](#8-conclusion)
9. [References](#9-references)

## 1. Introduction
Pairs trading is a market-neutral strategy in finance that capitalizes on the mean-reverting behavior of two correlated assets. When the relationship between two stocks diverges, traders can take a long-short position, betting that the two will realign. This project employs the Kalman Filter to adjust the hedge ratio dynamically, allowing for real-time trading strategy adjustments.

## 2. Background
The Kalman Filter is a recursive algorithm used for estimating variables of interest in real-time. In the context of pairs trading, the Kalman Filter provides an adaptive way to calculate the hedge ratio between two stocks. Instead of assuming a static relationship, the filter continuously updates this relationship as new data arrives, making it a robust tool for strategies that rely on changing market conditions.

## 3. Project Objectives
This project focuses on the following key objectives:
- **Understanding Pairs Trading:** Explore the theory and practice of pairs trading as a quantitative trading strategy.
- **Implementing the Kalman Filter:** Set up and implement the Kalman Filter to dynamically track and adjust hedge ratios.
- **Simulating Real-World Trading:** Apply the model to real-life stock data and simulate trades to evaluate strategy performance.
- **Avoiding Look-Ahead Bias:** Through the Bayesian nature of the Kalman Filter, ensure that the model avoids look-ahead bias and is suitable for backtesting.

## 4. Implementation Overview
The project consists of the following steps:
1. **Data Collection:** Collect historical data for two highly correlated stocks.
2. **Kalman Filter Setup:** Configure the Kalman Filter using the PyKalman library, initializing it with Bayesian parameters suitable for tracking stock relationships.
3. **Real-Time Adjustment of Hedge Ratio:** Use the Kalman Filter to dynamically update the hedge ratio, ensuring the pairs trading strategy remains responsive to market changes.
4. **Backtesting the Strategy:** Simulate historical pairs trading to assess the model’s effectiveness.
5. **Results Analysis:** Visualize and analyze results to see how well the Kalman Filter improves the trading strategy.

## 5. Requirements
To run this project, you’ll need the following:
- **Python 3.8+**
- **PyKalman:** For Kalman Filter implementation
- **Pandas:** For data manipulation
- **Matplotlib/Plotly:** For data visualization
- **Yahoo Finance API or yfinance library:** For obtaining stock data

You can install the required packages with:
```bash
pip install numpy pandas matplotlib pykalman yfinance
```

## 6. Code and Explanation
The code will include the following sections:
- **Data Collection:** : Uses yfinance to pull historical data on two correlated stocks, formatting it for the Kalman Filter.
- **Kalman Filter Model:** : The model initializes with parameters suited for financial time series, setting the observation matrix and covariance to track the hedge ratio.
- **Backtesting Strategy:** : Simulates historical pairs trades by triggering buy/sell actions when the price deviates from the calculated hedge ratio beyond a predefined threshold.
- **Visualization:** : Visualizes stock prices, hedge ratio changes, and trade signals, providing insights into model performance.

## 7. Conclusion
Through this project, I have created a pairs trading model that adapts to real-time data, helping to make trading strategies more responsive and market-aware. The Kalman Filter has proven effective at tracking hedge ratios, making this approach viable for real-world trading applications.
