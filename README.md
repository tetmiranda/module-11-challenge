# Module 11 Challenge
## Step 1: Find Unusual Patterns in Hourly Google Search Traffic
  1.1 Read the search data into a DataFrame, and then slice the data to just the month of May 2020
  
  1.2 Calculate the total search traffic for the month, and then compare the value to the monthly median across all months
    
## Step 2: Mine the Search Traffic Data for Seasonality
  2.1 Group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday)
   
  2.2 Using hvPlot, visualise this traffic as a heatmap, referencing index.hour for the x-axis and index.dayofweek for the y-axis. Does any day-of-week effect that you observe concentrate in just a few hours of that day?
   
  2.3  Group the search data by the week of the year. Does the search traffic tend to increase during the winter holiday period (Weeks 40 through 52)?
    
## Step 3: Relate the Search Traffic to Stock Price Patterns
  3.1 Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.
  
  3.2 Note that market events emerged during 2020 that many companies found difficult. But after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. So, slice the data to just the first half of 2020 (2020-01 to 2020-06 in the DataFrame), and then use hvPlot to plot the data. Do both time series indicate a common trend that’s consistent with this narrative?

  3.3 Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns:
  * “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility
  * “Hourly Stock Return”, which holds the percentage of change in the company stock price on an hourly basis

  3.4 Review the time series correlation, and then answer the following question: Does a predictable relationship exist between the lagged search traffic and the stock volatility or between the lagged search traffic and the stock price returns?

## Step 4: Create a Time Series Model by Using Prophet
  4.1. Set up the Google Search data for a Prophet forecasting model.
  
  4.2. After estimating the model, plot the forecast. How's the near-term forecast for the popularity of MercadoLibre?

  4.3. Plot the individual time series components of the model to answer the following questions:
  * What time of day exhibits the greatest popularity?
  * Which day of the week gets the most search traffic?
  * What's the lowest point for search traffic in the calendar year?
  
## Step 5 (Optional): Forecast the Revenue by Using Time Series Models
  5.1 Read in the daily historical sales (that is, revenue) figures, and then apply a Prophet model to the data.

  5.2 Interpret the model output to identify any seasonal patterns in the company revenue. For example, what are the peak revenue days? (Mondays? Fridays? Something else?)

  5.3 Produce a sales forecast for the finance group. Give them a number for the expected total sales in the next quarter. Include the best- and worst-case scenarios to help them make better plans.
