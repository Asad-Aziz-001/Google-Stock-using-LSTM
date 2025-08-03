# **📝 Notebook Summary: Stock Price Prediction using LSTM**

# **🔍 Objective**

The notebook aims to predict the future stock prices using deep learning techniques, specifically Long Short-Term Memory (LSTM) networks. LSTM is chosen due to its strength in capturing temporal dependencies in sequential data such as stock prices.

# **📊 Dataset Overview**

The dataset used contains historical stock price data (such as Open, High, Low, Close, and Volume).

The primary target for prediction is the "Close" price, which is typically used in financial forecasting.

# **⚙️ Data Preprocessing**

**Normalization:**
The price data is scaled using a normalization technique (likely MinMaxScaler) to bring values between 0 and 1. This helps the neural network train more efficiently.

**Sequence Creation:**
A sliding window approach is applied where the model uses a fixed number of past days (e.g., 60) to predict the next day’s closing price. This is essential for time series modeling.

**Train-Test Split:**
The dataset is split chronologically (not randomly) into training and testing portions, preserving the time-dependent nature of the data.

# **🤖 Model Architecture**

The model is based on LSTM layers, which are capable of learning long-term dependencies and patterns in time series data.

The model includes dropout layers to prevent overfitting and a dense output layer to produce the final prediction.

# **📈 Model Training**

The model is trained over multiple epochs on the training data.

Validation performance is monitored using metrics such as loss (Mean Squared Error).

A batch size is set to optimize training efficiency.

# **🧪 Prediction and Evaluation**

After training, the model is used to make predictions on the test data.

The predicted values are transformed back to original scale using the inverse of the normalization applied earlier.

# **Evaluation Metrics:**

MSE (Mean Squared Error) is calculated to quantify the average squared difference between predicted and actual values.

From the MSE value reported (≈1687), the RMSE is around (≈41.07), which indicates the average error in price prediction.

# **📊 Visualization**

A line graph is plotted comparing actual vs predicted stock prices on the test set.

This visual helps evaluate how closely the model tracks the real trend and any lag or deviation in predictions.

# **📌 Conclusion**

The LSTM-based model successfully learns temporal dependencies in stock prices and makes reasonably accurate predictions.
