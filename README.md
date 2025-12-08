# Dendri-Portfolio

## Multi-Output LSTM Forecasting for NYSE Time Series (1962–1986)
This project builds a single multi-output LSTM neural network to forecast:
Daily DJIA return
Log trading volume
Log volatility
based on the previous 5 trading days of historical features.
The model is trained on NYSE data from 1962–1986, standardized using training-set statistics to avoid look-ahead bias.

### Project Summary
- Built a sequential model with 2 LSTM layers (32 units each).  
- Predicts 3 outputs simultaneously.  
- Captures nonlinear relationships between returns, volume, and volatility.  
- Demonstrates stylized financial facts:  
  - Weak return predictability  
  - Volume–volatility correlation  
  - Strong volatility persistence  

<img width="443" height="337" alt="image" src="https://github.com/user-attachments/assets/526bf33b-c1e3-4c0a-939d-6f50ba8abf3c" />

### Why I Used This Data
The NYSE dataset (1962–1986) provides a long horizon of daily market activity, capturing multiple macroeconomic cycles, volatility  regimes, and behavioral patterns. It contains three variables that are central to quantitative finance:  
- Daily DJIA return – highly noisy but essential for understanding price movements.  
- Log trading volume – a proxy for market participation and liquidity.  
- Log volatility – a key input for risk models, VaR, and derivatives pricing.  
This makes the dataset ideal for building a multi-output time series predictor that captures how these variables interact dynamically.  
Instead of predicting each variable separately, I wanted a single unified model that learns the shared information structure across returns, volume, and volatility.  
This reflects real-world financial markets where:  
- Volume and volatility are strongly intertwined.  
- Volatility exhibits autocorrelation and clustering.  
- Returns are largely unpredictable but still influenced by market regimes.  
