

# Using LSTMS for Time Series Forecasting
File [Lstm_Predictions.ipynb](Lstm_Predictions.ipynb)

## Note:
1. I have used PM2.5 as the feature to be predicted as this is the most important parameter in air pollution, but we can predict any number of attributes just by making some adjustments to the code.


## Preprocessing Steps
1. I removed the columns with null points more than 40%.
2. Then imputed all the remaining null values with forward fill method.
3. Added timestamp column as index.


## Feature Engineering
1. Scaled all the columns using Standard scaler.
2. Added sin and cosine functions for different time intervals to capture seasonality in data.
3. Removed all the redudant columns.


## Model fitting
1. Provided an window size of 5 hours.
2. Defined an LSTM network and added two dense layers.
3. Used mean Squared error as loss, Adam as optimizer and Root Mean Squared error as evaluation metrics.


## Results
1. RMSE came about to be 20.5 for PM2.5 which is about 20% of mean of PM2.5.
2. Instead of using discrete data points to calculate error it would be better if we used a method like cumulative distribution function.


# Using LLMTIME by Nate Gruver et. al. 

I modified the demo.ipynb file in llmtime repository for our data. 
I was able to run the code for arima model. But for GPT models I was getting an error saying "local variable 'truncated_input_arr' referenced before assignment" inside some function. 
I haven't figured it out yet but will keep trying to solve the issue. 
My modified code can be found [here].(Using_llmtime.ipynb)

# Using OLLAMA
I have downloaded ollama on my local machine.
But there is still a long way to go to properly implement the llms for time series forecasting using OLLAMA.

Will update soon with more of good news. Peace out.
