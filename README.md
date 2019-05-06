# Algorithms

This repository contains the customized trading algorithms that I have created using the Quantopian IDE:

Visit https://www.quantopian.com/algorithms and copy/paste any of the algorithms to test!

Enjoy! ^_^

### The Futures Breakout Trading Model 
This was inspired by a book about the teachings of Richard Dennis and his trading partner Bill Eckhardt during the Turtle Experiment in 1983. The model trades ten different futures markets in an attempt to capture channel breakout patterns. In the experiment, they took 14 traders and taught them a complete rule-based trading system for determining markets, position sizing, entries, stops, exits, and a handful of miscellaneous (and useful) trading tactics that can be used to leverage different market nuances. Over the course of five years of trading, the Turtle group had reportedly earned more than $175 million. Visit http://bigpicture.typepad.com/comments/files/turtlerules.pdf for the complete book.  

### The Multi-Factor Model
This is the project that I dedicated myself to creating once I learned how to use Python to implement a trading model based on traditional financial theories. Factor investing is the idea of creating a portfolio that is weighted based on favorable factors such as quality, growth, value, momentum, and size (to name a few). A lot of research has been done and published regarding the concept of factor investing, so I thought to use my skills to develop a model that can be easily implemented and altered. When creating anything like this, I am sure to make it not only very user accessible, but also organized and visually aesthetic. As a note, the driving factor and strategy of this algorithm was researched before being backtested in the IDE. This algorithm was heavily influenced by my research notebook called: The Quality Score - Extracting 'Quality' From Your Pipeline 
https://github.com/brookswoolf/Trading-Algorithms/blob/master/Multi-Factor%20Model/The%20Quality%20Score%20-%20Extracting%20'Quality'%20From%20Your%20Pipeline.ipynb

### The Constrained Model 
This is an algorithm that I created using the defined contest criteria for Quantopian. This algorithm has more adjustable constraint and optimization settings compared to the Multi Factor Model simply because it is focused on those objectives. The Multi Factor Model is better for backtesting different alpha factor theories using different combinations of factors. The tested alpha factor from the Multi Factor Model can be easily plugged into this model and tested using the costrained criteria. This model can also be seen as a conservative approach to reviewing the actual strength of your alpha factor in a real world setting. The alpha factor was initially researched in this notebook: https://github.com/brookswoolf/Research-Notebooks/blob/master/Alpha%20Analysis.ipynb

### The Random Forest Regression Model 
This was something that I wanted to develop in order to better understand the application of machine learning in a quantitative finance. Although basic in its actual application, I feel like this helped me understand the actual objective that machine learning models try to accomplish. The idea of implementing trading strategies based on machine learning has been growing with popularity, however perfecting a model that relies heavily on a machine learned alpha vector is still very difficult even amongst seasoned professionals. That being said, I feel that this is the direction that we are headed, and in the near future this type of model is going to be implemented across all firms in the industry, some way or another. 

### Pairs Trading Model (US Equities)
This model serves as a framework to trade multiple pairs of cointegrated equities. Before plugging a pair into the backtesting environment, a recent time series of the relative returns should be tested for stationarity and normality, while their linear combination is ultimately tested for cointegration using a statsmodels cointegration test. After passing all of the tests in the research environment, the pair can be plugged into the trading model. A zscore is derived using the mean 21-day price spread between the pairs, it's standard deviation, and the current price spread between the pairs to be used for the trading logic. In its current state, the model is purely a framework for backtesting new research.

### Monthly Momentum Model
I developed this model in response to an inquiry on the Quantopian forums. A user was inquiring how to incorporate a double sort technique to rank and order stocks in the pipeline based on monthly returns. The positive (negative) sign of cumulative monthly returns is used as a pre-filter for the long (short) baskets. Stocks are continuously ranked based on 21-day returns (average amount of trading days per month). Stocks in the long basket with the highest 21-day returns are bought long, and stocks in the short basket with the lowest 21-day returns are sold short. The portfolio is set up to be dollar neutral and rebalances once a month. Post links: https://www.quantopian.com/posts/help-with-custom-factor-1#5ca63355ef3ace1c54ccd5f4 and https://www.quantopian.com/posts/help-with-custom-factor-1#5ca6c0531abbaa321f790e34 

