# Name
Time series prediciton on Vegetables and Fruits price

# Data
The resoucre of the data is from Kaggle website (https://www.kaggle.com/datasets/ramkrijal/agriculture-vegetables-fruits-time-series-prices/data), and it named Time Series Price Vegetables and Fruits

# Prophet
Training based on the target label value and testing with other data to conduct sentiment analysis.It is almost the same as the general text-based classification.

We used the Prophet library to forecast time series data for commodity prices. The dataset included columns such as Commodity, Date, Unit, Minimum, Maximum, and Average. We focused on predicting the Average price over time for a selected commodity. The process involved:

    Data Preparation: Filtered the dataset for a specific commodity and reformatted it to include only the Date and Average columns, renaming them to ds (date) and y (value), as required by Prophet.

    Model Training: Initialized and trained a Prophet model using the prepared data.

    Future Forecasting: Created a future dataframe to predict prices for the next 12 months.

    Visualization: Plotted the forecasted prices along with confidence intervals and analyzed the forecast components, such as trend and seasonality.

    Results: Generated a forecast containing predicted prices (yhat) with lower and upper confidence intervals for the specified time period.


# EDA, Feature Engineering, Parameter 