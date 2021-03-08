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

In my research I tried to understand  stock prices movements based on technical indicators (Returns, MACD and Signal, Rolling mean and standard deviation, RSI ) . The objetive was to know the main trading parameters within the finantial environment and see the evolution during these last months for main pharma companies with Covid19 vaccine
On the other hand I tried to apply some deep learning models for stock prices of two of these pharma comapanies since it seems that they are working really well on time series analysis of other kind of fileds.
I've learnt the importance to normalize data before use a LSTM or GRU models (Recommendation from many sources si to use a range between -1 and +1) and also the possbility we have to make predictions for one day (many to one) or for many days (many to many) but in any case I need to have more knowledge about this topic if my goal was to invest my money based on my analysis/models.
Taking into account all this and based on RMSE and processing time I have the best results with GRU architecture comparing with LSTM

### Evolution and Volatility:

#### Pfizer Evolution

![Evo_Rolling_Pfizer_V1](https://user-images.githubusercontent.com/46485715/110109017-3233c580-7dad-11eb-91cf-21318f0c83e3.png)

#### Astra Zeneca Evolution:

![Evo_Rolling_AstraZeneca_V0](https://user-images.githubusercontent.com/46485715/110109036-3829a680-7dad-11eb-80d0-42fe17944ce3.png)




### Deep Learning:
Comparing the performance and results between LSTM and GRU Networks show GRU as the winner in both cases

#### LSTM Results:

![Result_LSTM_Pfizer_V0](https://user-images.githubusercontent.com/46485715/110108226-30b5cd80-7dac-11eb-91f7-e2c3e081f75f.png)


#### GRU Results, with same hyperparameters:

![Result_GRU_Pfizer_V0](https://user-images.githubusercontent.com/46485715/110108357-6064d580-7dac-11eb-9dba-a2b13caf2b90.png)

## Results
The main findings of the code can be found at the Medium blog post available [here](https://medium.com/p/85d9b2c9a255/edit)

## Improvements:

In order to improve the prediction performance of the models is important to change the way I have standardized the data to train the model, only the training data have to be used to fit the scaler transformation, then the scaler is used to transform the test input data. In the models I'm sharing on this blog probabily there is a bias due to I have standarized train and test datarset.
Avoid Overfitting .The real issue is that overfitting not only makes your model inefficient, it could make your prediction very wrong. Deep learning uses the dropout technique to control overfitting. The dropout technique randomly drops or deactivates some neurons for a layer during each iteration. It is like some weights are set to zero. So in each iteration the model looks at a slightly different structure of itself to optimize the model.   
Do the same exercise based on Keras in order to consolidate the knowlegde about how LSTM networks work
Try to make predictions not over "Close" but over "Returns"  

## References:

https://github.com/ranaroussi/yfinance  
https://www.investopedia.com  
https://machinelearningmastery.com/how-to-develop-lstm-models-for-time-series-forecasting  

 
