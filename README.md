# Tech-stock-performance
Stock analysis of driving tech stocks over the period of 5 years between 2019 and 2024
#install yfinance if already installed
!pip install yfinance

import yfinance as yf
import pandas as pd
import matplotlib.pyplot as plt

#download historical data for tech stocks
historical_data= yf.download (["NVDA", "MSFT", "PLTR", "BABA", "NOW"], period="5y")

#display first 5 rows
print(historical_data.head())

plt.figure(figsize=(10,5))
plt.plot(historical_data['Close'])
plt.title("NVDA, MSFT, PLTR, BABA, NOW Stock Closing Price (Last 5y)")
plt.xlabel("Date")
plt.ylabel("Price (USD)")
plt.show()
