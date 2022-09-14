# Key_Market_Crash_Indicators_And_Optimal_Portfolio
In this analysis we examine several key indicators typically associated with stock market crashes. In this assignment we assume the definition of a market crash as "an abrupt drop in stock prices, which may trigger a prolonged bear market or signal economic trouble ahead" (Investopedia). The scope of our examination will include four timeframes typically identified as a "crash": the dotcom bubble in the early 2000's, the real estate bubble of 2008, the Covid19 pandemic period, and the present market conditions. After examining these key indicators such as GDP, Unemployment, Industrial Productions, Inflation, and Fedfunds we will take a look at our current market to see if there are any commonalities that might indicate a coming recession or crash. For each period we will also be looking at what sectors perform well in the SP500 during these market crash conditions to attempt to indentify sectors that may be worth investing in during market crashes or bear markets.

## Libraries and Dependencies

import os - creating and removing directory
import requests - send http request
import pandas as pd - imports pandas library
from pathlib import Path - reading in csv files
import alpaca_trade_api as tradeapi - accessing alpaca api
from dotenv import load_dotenv - loading in env files for api usage
import hvplot.pandas - plotting data
import math - provides functions that are useful for math problems
from MCForecastTools import MCSimulation
import matplotlib.pyplot as plt
import numpy as np
import seaborn as sns
%matplotlib inline - creating visualizations

## Technologies
You will need the following csv data for the project: Combined_Sectors_df which containes historical data for the 11 sectors of the SP500. This dataframe will be used for each different df. The following csv files are key indicator data which include: FEDFUNDS.csv, GDP2.csv, INDPRO.csv, inflation.csv, UNRATE.csv. MCForecastTools library must also be in your repository to run MonteCarlo Forecast.

## Table of Contents
Dotcom bubble Analysis of the 11 sectors of the SP500
    1. Analyze the crash and charts
    2. Key indicators data
    3. What sectors of the SP500 performed well
Real Estate Bubble of 2008/09
    1. Analyze the crash and charts
    2. Key indicators data
    3. What sectors of the SP500 performed well
Covid19 Pandemic Period
    1. Analyze the crash and charts
    2. Key indicators data
    3. What sectors of the SP500 performed well
Current Market Condition
    1. Analyze the current market and charts
    2. Key indicators data
    3. What sectors are performing well
Do the key indicators identify a possible market crash in our current period based on prior crashes
    1. Is a possible market crash coming?
    2. If so, What ETF's should I invest in?
    3. Plot daily returns if those sectors were held during the real estate bubble
    4. Run MonteCarlo simulation of a possible portfolio which includes these ETF's

## Sources used for project and analysis
https://fred.stlouisfed.org was used for the key indicators data.
https://www.investopedia.com/terms/s/stock-market-crash.asp#:~:text=A%20stock%20market%20crash%20is%20an%20abrupt%20drop%20in%20stock,among%20panicked%20investors%20to%20sell was used for market crash definitions.
https://www.sectorspdr.com/sectorspdr/tools/sector-tracker/charting was used for sector data of the SP500.