# DSND-Cpastone_Pharma_Stocks

![Vaccine_V1](https://user-images.githubusercontent.com/46485715/110025790-2229d080-7d30-11eb-8090-9fc90969d12d.jpg)



## Project Overview:

In my capstone project I am exploring the movements of stock prices creating traditional finantial varialbes (MACD, RSI, Rolling Averages) and applying some machine learning technics, trying to predict the movements of stock prices only for educational reasons

Data I use is from yahoo finance. As input I take daily trading data: opening price (Open), highest price the stock traded at (High), how many stocks were traded (Volume) and closing price adjusted for stock splits and dividends (Adjusted Close).

First I am looking at the development of adj close stock prices by means of comparing a visualising different trading parameters: Daily returns, Cumulative returnes, Rolling statistics of mean, standard deviation and Bollinger Bands, as well as MACD and RSI. These parameters show, how risky (or volatile) are the stock prices, how profitable they are and what investing logic could be used. Several of these techniques indeed have some power to predict stock prices movements.

After looking at the trading parameters, I am going forward in my analysis of stock prices movements by means of machine learning models. 

## Installations:
Inorder to get the stock market information you need to pip install yfinance

pip install yfinance (https://github.com/ranaroussi/yfinance or https://pypi.org/project/yfinance/)

My project is using the following libraries:

pandas  
numpy  
random  
matplotlib  
seaborn
torch
sklearn  
ploty


## Summary:
In my research I create financial varibles in order to see the evolution, returns, volatility of the stock prices and also I tried to use Deep Learning Models looking for a prediction of these values or at least a prediction for the movements considering the risk of overfitting in this kind of exercises.

Comparing the performance and results between LSTM and GRU Networks show GRU as the winner in both cases




 
