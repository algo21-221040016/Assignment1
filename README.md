This is the first assignment for algorithm trading, and in this assignment, I tried to use LSTM and RNN to forecast the price of MaoTai stock.

*Introduction
The biggest difference between RNN, recursive neutral network, and other traditional neutral network is that RNN connects with sequence.But RNN has a big problem about long-term dependencies, and this is actually a vanishing-gradient problem. LSTM, long-short term memory, is used to solve this kind of problem.  The difference between LSTM and traditional RNN exists in hidden layers.
In this assignment, i used LSTM model in single time step and recursively call it.

*About the code
1. data: i downloaded the stock prices of MaoTai from tushare, and use the data from year 2014 and year 2017 as the training set  and the data in year 2018 as test set. Actually we can also use tushare with python directly. Then, I preprocessed the raw data with steps such as standardization and 
feature scaling.
2. model training: in this stage, i chose the close price as the input feature in neutral network and then trained the stochastic bias and weights of neutral network. The chosen optimizer will influence the convergence rapidity of the model and in this assignment i chose Adam optimizer. To avoid over-fitting, i added Dropout into the model.
3. The last step is visualizing the results.

*Analysis about the model and improvements:
The prediction of LSTM model shows a lag and it's obvious that machine learning method can not predict the sudden change of stock price which may be caused by the company or other reasons.To predict the stock price more precisely, GNN is now applied into use and echo network is also a way to solve the  problem of chaotic sequence prediction.
