# Nifty50 prediction model (LSTM)
This project uses a long short-term memory (LSTM) model to predict the Nifty50 stock index price based on the 100-day and 200-day rolling averages. The model was trained on data from 2008 to 2023 using pandas, matplotlib, TensorFlow, and Keras.

## Data
The data used in this project is historical daily data for the Nifty50 index from 2008 to 2023. The data was obtained from www.marketwatch.com and contains the following columns:

* Date: the date of the observation
* Open: the opening price of the index
* High: the highest price of the index during the day
* Low: the lowest price of the index during the day
* Close: the closing price of the index

## Model
The LSTM model was built using TensorFlow and Keras. There are 4 LSTM layes, each having a specified number of units, which determines the dimensionality of the output space. The activation function used in each LSTM layer is ReLU, which is commonly used in deep learning models. The output of each LSTM layer is passed through a dropout layer, which randomly drops out a specified fraction of the units to help prevent overfitting.

The model was trained using mean squared error (MSE) as the loss function and the Adam optimizer. The training data consisted of the rolling averages and corresponding Nifty50 prices for the period from 2008 to 2019, and the validation data consisted of the same for the period from 2019 to 2023.

## Results
While the model did not predict the exact Nifty50 prices, it was able to predict the trend accurately. Specifically, it was able to predict whether the index would go up or down on a given day based on the rolling averages.

This can be seen in the following figure, which shows the actual and predicted trends for the validation period:

![image](https://user-images.githubusercontent.com/29772969/228191676-2dccc7e2-88a3-45c2-992d-baa0dace81dc.png)


As you can see, the model was able to capture the overall direction of the Nifty50 index, even if the exact prices were not predicted. This can still be useful for making informed investment decisions and identifying potential opportunities in the market.

Future work could explore ways to further improve the model's accuracy in predicting the exact prices, such as incorporating additional features or experimenting with different model architectures.

## Conclusion
In this project, we demonstrated how an LSTM model can be used to predict Nifty50 prices based on rolling averages. While the model's performance was not perfect, it did achieve reasonable accuracy in predicting the index's price movements. There are certainly many avenues for future improvement, including incorporating additional features into the model or experimenting with different architectures altogether.
