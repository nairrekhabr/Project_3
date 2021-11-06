# **Comparative Analysis of Mutual Funds and Cryptocurrencies**

## **About**

This project aims to build a comparative study of popular S&P 500 mutual funds, target 2040 retirement funds, & cryptocurrencies. Our analysis consists of a comparison of historical performance and volatility, as well as a comparison of projected future performance.

The results of our comparative analysis were then used to build an investment advisor based on risk appetite.

### **Mutual Funds in Comparison**:
Below are the mutual funds we focused on for our comparative study:
- Vanguard (VOO, VFORX)
- Fidelity (FXAIX, FFFFX)
- T. Rowe Price (PREIX, TRRDX)
- Schwab

### **Cryptocurrencies in Comparison**:
Below are the cryptocurrencies included in our comparative analysis:
- Bitcoin (BTC)
- Litecoin (LTC)
- Ripple (XRP)
- Ethereum (ETH)
- Maker (MKR)
- Chainlink (LINK)
  
### **Comparison Metrics**:
- Average Annualized Return
- Standard Deviation
- Sharpe Ratio
- Sortino Ratio
- R2 Ratio
- Alpha Ratio
- Beta Ratio
  
### **Prediction Methods**:
- Linear Regression
- Average Annualized Return


## **Technology Stack**

Python, Pandas, Hvplot, Numpy, Linear Regression (sklearn), YFinance API, CoinGecko API

### **Installations**:

1) [Yahoo Finance](https://pypi.org/project/yfinance/): Used to pull historical data for mutual funds in analysis.
- Run the following command at terminal to install:
    
    `pip install yfinance`
- Import command:

    `import yfinance as yf`

2) [CoinGecko API](https://github.com/man-c/pycoingecko): Used to pull historical data for cryptocurrencies in analysis.
 
- Run the following command at terminal to install:
    
    `pip install pycoingecko`
- Import command:

    `from pycoingecko import CoinGeckoAPI`


## **Screenshots**
---
### Mutual fund SP500

<img width="583" alt="Comparative Analysis SP500" src="https://user-images.githubusercontent.com/83980061/140423531-13818120-2274-42df-bf67-c6b143216883.png">

### Target Retirement fund 2040

<img width="572" alt="Comparative Analysis Target Retirement fund 2040" src="https://user-images.githubusercontent.com/83980061/140423546-98551e35-839f-4b8e-bb24-14bae8155a89.png">

---
### **Crypto Analysis**:

We compared various return and volatility metrics to assess the historical performance of the cryptocurrencies in our analysis. Our calculations are based on historical closing price data from the last 1,000 trading days. 

#### 1) **Comparison of Cumulative Returns**
![Cumulative Returns Comparison](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/crypto_cumltv_returns_hv.png)

From a cumulative return perspective, Chainlink (LINK) and Ethereum (ETH) are clearly the strongest performers over the las 1,000 trading days, with LINK experiencing particularly explosive growth over the period. At the same time, the above plot also highlights significant volatility in LINK's returns.

Bitcoin (BTC) showed relatively strong growth over the same timeframe. While the other assets in the comparison experienced respectable growth, they all underperformed the sector benchmark (BTC).

#### 2) **Comparison of Average Annualized Returns**
![Average Annualized Returns](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/annlzd_returns_plot.png)

The comparison of average annualized returns tells a similar story to the cumulative returns comparison. LINK (~170%) and ETH (~125%) provided the highest annualized average return. Interestingly, Maker (MKR), which did not produce a significant cumulative return relative to the other assets, provided an average annualized return of roughly 107% over the last 1,000 trading days.

As with the cumulative returns comparison, Ripple (XRP) and Litecoin (LTC) underperformed BTC in the annualized return comparison.

#### 3) **Comparison of Return Volatility**
![Annualized Volatility](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/annlzd_vol_plot.png)

 Chainlink and Maker stand out as the two most volatile assets in the comparison. Unsurprisingly, the two leading and most established cryptocurrencies, ETH and BTC, produced the least volatile returns.


#### 4) **Sharpe Ratio & Sortino Ratio Comparison** 
 To assess the risk-adjusted returns of the assets, we calculated and compared the respective Sharpe ratios.

![Sharpe Ratio](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/sharpe_ratio_plot.png)

Based on the Sharpe ratio comparison, ETH, LINK, & BTC are clearly the best investments on a risk-adjusted basis. Maker also appears to be a strong risk-adjusted investment; MKR has a Sharpe ratio close to 1.

To expand on our risk-adjusted analysis, we calculated and compared the cryptocurrencies' Sortino ratio. The Sortino ratio isolates for downside risk, and therefore, focuses on the impact of downside volatility on returns.

![Sortino Ratio](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/sortino_ratio_plot.png)

The Sortino ratio comparison did not offer any new insights; ETH, LINK, & BTC still produce the best risk-adjusted returns.

#### 5) **Beta Comparison**
We used the S&P 500 (SPY) as our benchmark for the Beta calculation.

![Beta](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/beta_plot.png)

The key takeaway from the beta comparison is that all of the cryptocurrencies in our analysis are inversely correlated with the broader stock market. This suggests that cryptocurrencies could be potentially be used to hedge portfolios that are heavily weighted toward index ETFs and/or leading stocks.


#### **Summary of Historical Returns & Volatility Metrics**
![Crypto Metrics Summary](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/full_metrics_table.png)

#### **Estimated Future Growth**:

In addition to the historical analysis, we estimated future growth to assess the potential upside of investing in each cryptocurrency. We used two methods to estimate future growth:

1) All-Time Average Annualized Return
2) 10-year, 1,000 Path Monte Carlo Forecast

Under the first approach, we simply calculated the all-time average annualized return for each asset, and used this rate to extrapolate 5 and 10-year growth rates:

![Annualized Return Forecast](https://github.com/nairrekhabr/Project_3/blob/main/combined_crypto_analysis/images/annlzd_return_fcst.png)

This results of this simple forecast based on the all-time average annualized return indicate that LINK and ETH offer the most upside for future growth.

To generate another point of reference for our forecasting, we also ran 10-year, 1,000 path Monte Carlo forecasts for BTC, ETH, LINK, and XRP. To quantify the Monte Carlo results, we estimated the 95% confidence intervals and median expected values of an initial investment of $10,000.

While the magnitude of the Monte Carlo forecasted growth differed from the previous approach, the conclusions were the same; LINK and ETH still offer the greatest upside for future growth:

![BTC_XRP_MC ](https://github.com/nairrekhabr/Project_3/blob/main/btc_xrp_analysis/images/btc_xrp_ci_median_summ.png)
![ETH_LINK_MC ](https://github.com/nairrekhabr/Project_3/blob/main/eth_link_analysis/images/eth_link_fcst_ci_median_summ.png)

#### **Conclusions: Cryptocurrency Analysis**

Based on our analysis, we decided to remove LTC & XRP from our list of recommended investments. LTC and XRP do not appear to offer returns sufficient enough to compensate investors for increased volatility. Additionally, XRP in particular does not seem to offer significant upside for future growth.

We ultimately decided that a conservative investor's cryptocurrency portfolio should be mostly comprised of BTC and ETH. Our analysis showed that BTC & ETH are the least volatile assets in our comparison, and also provide strong risk-adjusted returns. Moreover, as the two leading and most established cryptocurrencies, we believe BTC & ETH are likely to have significant staying power going forward.

For investors with a greater appetite for risk, we recommend expanding their crypto portfolios to incorporate Chainlink and Maker, in addition to Ethereum and Bitcoin. Chainlink in particular has displayed a track record of providing significant risk-adjusted returns, while also providing investors with significant upside for future growth.

---
## Contributors

- John McGraw @mcgrawj012
- Nikhil Golthi @Nik-Golthi
- Michel Nagle@mrnaglejr
- Joseph Arewa @jarewa2
- Hillary Hwaga @Hillhwaga
- Sravani Misra @Sravani Misra
- Rekha Ramachandran @nairrekhabr




