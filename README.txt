Automated Electricity trading strategy.

This repository contains code for analyzing electricity auctions data and developing a trading strategy based on the analysis. The data used in this project comes from the UK electricity market.

# Setting Up
The repository has been tested on Python 3.8.13 and external Python libraries used in this repository are:

Pandas 1.5.3
Numpy 1.23.5
Matplotlib 3.7.1
statsmodels 0.13.5
sklearn 2.6.0
xgboost 1.7.3

A brief description of Python script and the data file is provided below:

File : Description 
Electricity Auction Analysis.ipynb:  This Jupyter Notebook contains the code for analyzing electricity auction data and the trading strategy.
auction_data.csv: Containing the actual prices and volumes traded in both auctions and a price forecast for the first auction.
system_prices.csv: Containing the system prices and the forecasted price range of the system.
forecast_inputs.csv: Containing the necessary input variables that can be utilized for predicting the prices of the second auction. 
description_input_variables.txt : Further details about these input variables.

# Copyright

Copyright (C) 2023 Moh'd Khier Al Kfari
