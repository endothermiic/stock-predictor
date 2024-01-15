# Using a CNN-LSTM model to predict stock performance

The start of this notebook contains important financial metrics such as:
* 10-day exponential moving average
* Daily return percentage
* Adjusted closing price
for 5 unique stocks (ADI, AMD, IBM, NVDA, ON - can you tell I enjoy hardware?).

A list of all companies available for analysis from the S&P500 was exported from [Wikipedia](https://en.wikipedia.org/wiki/List_of_S%26P_500_companies) and can be found in the file `s&p500.csv` - users wishing to change the stocks or number of stocks displayed can modify `stocks_list` in `stock-predictor.ipynb` with any stocks in the list `symbols` (this is a full list of stocks in Python extracted from the .csv) of their choosing.

The remainder of this notebook contains data pre-processing, model training and final testing. A CNN-LSTM (convolutional neural network, long short-term memory) model was used for the model with 5 kernals (this significantly reduced loss relative to 3 or 7). MSE was chosen over MAE to evaluate loss since few outliers were observed in the original dataset for these 5 stocks. There was a 70/10/20 split for training/validation/test data respectively. 

**Note:** Users wanting to experiment can modify the kernal size, number of epochs, batch size and loss metric to observse how the max error, R^2 and loss plots change. The final result of the model as of now is shown below:

<img width="490" alt="image" src="https://github.com/endothermiic/stock-predictor/assets/103846051/c2bf644d-5d9d-46e2-9cc8-dbd0c728760d">
