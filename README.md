# Stock_Market_Analysis
## Introduction
1)Understand why would you need to be able to predict stock price movements;

2)Download the data - You will be using stock market data gathered from Yahoo finance;

3)Split train-test and validation data and also perform some data normalization;

4)Motivate and briefly discuss an LSTM model as it allows to predict more than one-step ahead;

5)Predict and visualize future stock market with current data


**Note: Stock market prices are highly unpredictable and volatile. This means that there are no consistent patterns in the data that allow you to model stock prices over time near-perfectly.**


## Downloading the Dataset
Dataset Link : https://finance.yahoo.com/quote/NTPC.NS/history?p=NTPC.NS


## Important terms to make insights from Stock Data

Stock prices come in several different flavors. They are,

Open: Opening stock price of the day

Close: Closing stock price of the day

High: Highest stock price of the data

Low: Lowest stock price of the day

## Introduction to LSTMs: Making Stock Movement Predictions Far into the Future

Long Short-Term Memory models are extremely powerful time-series models. They can predict an arbitrary number of steps into the future. An LSTM module (or cell) has 5 essential components which allows it to model both long-term and short-term data.
Cell state (ct) - This represents the internal memory of the cell which stores both short term memory and long-term memories
Hidden state (ht) - This is output state information calculated w.r.t. current input, previous hidden state and current cell input which you eventually use to predict the future stock market prices. Additionally, the hidden state can decide to only retrive the short or long-term or both types of memory stored in the cell state to make the next prediction.
Input gate (it) - Decides how much information from current input flows to the cell state
Forget gate (ft) - Decides how much information from the current input and the previous cell state flows into the current cell state
Output gate (ot) - Decides how much information from the current cell state flows into the hidden state, so that if needed LSTM can only pick the long-term memories or short-term memories and long-term memories
