# Project Title - Forecasting_Net_Profit

## Introduction
As a growth analyst at Mercadolibre, the primary objective of our team is help the company grow by analyzing the company's financial and user data and if the ability to predict search traffic can translate into the ability to successfully trade the stock. 

## Technologies
**Python Libraries**

`python 3.9.12`<br>
`pandas 1.4.2`<br>
`Prophet`<br>
`hvplot 0.73`<br>
`pystan`<br>
`holoviews`

## Installation Guide

[Install Anaconda](https://www.anaconda.com/download/)

To clone and run this application, you'll need Git installed on your computer.
From your command line:
```
#Create a new conda environment
conda create -n dev python=3.7 anaconda

#Activate the new environment with the following command
conda activate dev

# Install dependencies in the new conda environment
pip install jupyter lab
pip install pystan
pip install prophet
pip install panel hvplot
pip install holoviews
conda install -c pyviz hvplot

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

The steps for this challenge are broken out into the following sections:

1.) Find unusual patterns in hourly Google search traffic.<br>



2.) Mine the search traffic data for seasonality.<br>

3.) Relate the search traffic to stock price patterns.<br>

4.) Create a time series model with Prophet.<br>


## Contributors
- Firas Obeid, UC Berkeley FinTech Instructor
[GitHub](<https://github.com/firobeid>)
- Lavina Tang, UC Berkeley FinTech Tutoring Team
[LinkedIn Profile](<https://www.linkedin.com/in/lavinamahoney>)
- Alexander Valenzuela<br>
[LinkedIn Profile](<https://www.linkedin.com/in/alex-valenzuela-97826842/>)


## License
Licensed under the MIT License

