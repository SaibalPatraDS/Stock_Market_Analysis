# Stock Market Analysis using LSTM

## Team Members : 

1) GIRIRAJ - **2020UCA1904**
2) VINEET KUMAR - **2020UCM2312**
3) SAIBAL PATRA - **2020UCM2348**

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

![image](https://user-images.githubusercontent.com/102281722/186481557-6f2553ee-08ea-418c-baa4-5fb49dfae5fd.png)

## Splitting the Data

For the model, we have partitioned the dataset into three parts, Training, Validation, and Testing section.

Training section consists of 80% of the data.

Validation part contains the data present in between 80 and 90%

For testing we will use the rest of the data.

## LSTM Model

For training the model, we are using LSTM algorithm.

We are using the Sequential model, Adam optimizers, and fixing the learning rate to 0.001.

We will run the model for 100 times(epoch = 100)

## Visualizing the Data

We will visualize Training Predictions and Observations, Testing Predictions and Observations, and Validation Predictions and Observations one by one. 

Training Dataset Visualization 
![image](https://user-images.githubusercontent.com/102281722/186483438-329837cf-fdc1-4efd-8228-bca3ac10afa0.png)

Testing Dataset Visualization 
![image](https://user-images.githubusercontent.com/102281722/186483615-fd9233b4-83f5-4fd3-9b64-5cf60bf11359.png)

Validation Dataset Visualization
![image](https://user-images.githubusercontent.com/102281722/186483697-f74be258-1f3f-4ac0-80bf-274ad1a3fcd3.png)

Visualization of the entire data
![image](https://user-images.githubusercontent.com/102281722/186483794-9ccc32e3-ee53-4964-96f4-b2ad26a1e148.png)




