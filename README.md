# Project Title - Forecasting Net Prophet

## Introduction
As a growth analyst at Mercadolibre, the primary objective of our team is help the company grow by analyzing the company's financial and user data and if the ability to predict search traffic can translate into the ability to successfully trade the stock. 

## Technologies
**Python Libraries**

`python`<br>
`pandas`<br>
`numpy`<br>
`hvplot`<br>
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
from prophet import Prophet
import panel as pn
import hvplot.pandas
import holoviews as hv
import datetime as dt
%matplotlib inline
import pandas as pd
import numpy as np

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
![Screenshot 2023-06-05 at 8 18 34 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/b16b8f57-cab8-45a9-8cb9-0d96e0cb7800)
- Calculate the total search traffic for the month, and then compare the value to the monthly median across all months.<br> 


2.) Mine the search traffic data for seasonality.<br>
- Group the hourly search data to plot the average traffic by the day of the week (for example, Monday vs. Friday).<br>
- Using hvPlot, visualize this traffic as a heatmap, referencing the `index.hour` as the x-axis and the `index.dayofweek` as the y-axis.<br> 
![Screenshot 2023-06-05 at 8 29 18 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/40be17a4-be49-4f4f-b169-28737a7606da)
- Group the search data by the week of the year.<br>
![Screenshot 2023-06-05 at 8 30 45 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/8433a091-38bd-47e1-91d2-2bcff0e3b78b)


3.) Relate the search traffic to stock price patterns.<br>
- Read in and plot the stock price data. Concatenate the stock price data to the search data in a single DataFrame.<br>
![Screenshot 2023-06-05 at 8 07 56 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/6980882e-611d-4629-a075-9989203a7644)
- Market events emerged during the year of 2020 that many companies found difficult. But, after the initial shock to global financial markets, new customers and revenue increased for e-commerce platforms. Slice the data to just the first half of 2020 (`2020-01` to `2020-06` in the DataFrame), and then use hvPlot to plot the data.<br> 
![Screenshot 2023-06-05 at 8 08 35 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/8ba98d95-33d5-422a-b821-fda620cb193f)
- Create a new column in the DataFrame named “Lagged Search Trends” that offsets, or shifts, the search traffic by one hour. Create two additional columns: “Stock Volatility”, which holds an exponentially weighted four-hour rolling average of the company’s stock volatility and “Hourly Stock Return”, which holds the percent change of the company's stock price on an hourly basis.<br>
![Screenshot 2023-06-05 at 8 11 42 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/5ca3aab5-171e-496a-a19f-84b7639588e9)
- Review the time series correlation.<br> 
![Screenshot 2023-06-05 at 8 16 34 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/77c1dbd9-65b1-424c-aa2c-0a17085b2da2)


4.) Create a time series model with Prophet.<br>
- Set up the Google search data for a Prophet forecasting model.<br>
- After estimating the model, plot the forecast.<br> 
![Screenshot 2023-06-05 at 7 53 05 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/b65745f2-d750-4aa6-9797-4afbcb8ec792)
- Plot the individual time series components of the model.
![Screenshot 2023-06-05 at 8 02 25 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/308324f3-2303-4c38-869f-7ba91bd9a185)

 ![Screenshot 2023-06-05 at 7 54 11 PM](https://github.com/AlexanderValenzuela/Forecasting_Net_Prophet/assets/111409358/43d400c7-5636-4006-8c4b-32568634696d)


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

