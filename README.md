# Project Title - Forecasting Net Prophet

## Introduction
As a growth analyst at Mercadolibre, the primary objective of our team is help the company grow by analyzing the company's financial and user data and if the ability to predict search traffic can translate into the ability to successfully trade the stock. 

## Technologies
**Python Libraries**

`python 3.9.12`<br>
`pandas 1.4.2`<br>
`hvplot 0.73`<br>
`prophet`<br>
`holoviews`<br>
`%matplotlib inline`<br>
`datetime`


## Installation Guide
```
# Run Jupyter Notebook in Google Colab 
```
[forecasting_net_prophet.ipynb](https://colab.research.google.com/drive/1RPIs40nvPPHu7vnCBMvmiJAo1r1ZmQkQ#scrollTo=5d5IDtwSK3q7)
```
# Install the required libraries
!pip install pystan
!pip install prophet
!pip install hvplot
!pip install holoviews

# Import the required libraries and dependencies
import pandas as pd
import holoviews as hv
from prophet import Prophet
import hvplot.pandas
import datetime as dt
%matplotlib inline

# Clone this repository on your local machine
git clone https://github.com/AlexanderValenzuela/forecasting_net_prophet

# Activate conda environment
conda activate dev

# In the conda environment, run Jupyter Lab
jupyter lab 

# Browse to the crypto_investments directory and launch `forecasting_net_prophet`
```
---

## Usage

Forecasting Net Prophet

This section divides the instructions into five steps as follows:

1.) Find unusual patterns in hourly Google search traffic.<br>
- Read the search data into a DataFrame, and then slice the data to just the month of May 2020. (During this month, MercadoLibre released its quarterly financial results.) Use hvPlot to visualize the results.<br>
- Calculate the total search traffic for the month, and then compare the value to the monthly median across all months.<br> 

2.) Mine the search traffic data for seasonality.<br>
- Group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday).<br>
- Using hvPlot, visualize this traffic as a heatmap, referencing the `index.hour` as the x-axis and the `index.dayofweek` as the y-axis.<br> 
- Group the search data by the week of the year.<br>

3.) Relate the search traffic to stock price patterns.<br>
- Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.<br>
- Market events emerged during the year of 2020 that many companies found difficult. But, after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. Slice the data to just the first half of 2020 (`2020-01` to `2020-06` in the DataFrame), and then use hvPlot to plot the data.<br> 
- Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns: “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility
and “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis.<br>
- Review the time series correlation. 

4.) Create a time series model with Prophet.<br>
- Set up the Google search data for a Prophet forecasting model.<br>
- After estimating the model, plot the forecast.<br> 
- Plot the individual time series components of the model.

5.) Forecast Revenue by Using Time Series Models
- Read in the daily historical sales (that is, revenue) figures, and then apply a Prophet model to the data.<br>
- Interpret the model output to identify any seasonal patterns in the company's revenue.<br>
- Produce a sales forecast for the finance group. Give them a number for the expected total sales in the next quarter. Include the best- and worst-case scenarios to help them make better plans.<br>


## Contributors
- Firas Obeid, UC Berkeley FinTech Instructor
[GitHub](<https://github.com/firobeid>)
- Lavina Tang, UC Berkeley FinTech Tutoring Team
[LinkedIn Profile](<https://www.linkedin.com/in/lavinamahoney>)
- Alexander Valenzuela<br>
[LinkedIn Profile](<https://www.linkedin.com/in/alex-valenzuela-97826842/>)


## License
Licensed under the MIT License

