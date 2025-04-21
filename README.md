# Cryptocurrency Trading Strategy Analysis

## Project Overview
This repository contains a comprehensive analysis of cryptocurrency trading strategies using technical indicators, specifically focused on Ethereum (ETH). The project demonstrates how to leverage moving average crossover strategies to make trading decisions in the cryptocurrency market.

## 📊 Key Features

- **Historical Data Analysis**: Fetching and processing cryptocurrency historical data using both Historic_Crypto API and Binance API
- **Technical Indicator Implementation**: Calculating Simple Moving Average (SMA) and Exponential Moving Average (EMA)
- **Signal Generation**: Creating buy/sell signals based on SMA/EMA crossovers
- **Backtesting Framework**: Evaluating trading strategy performance against buy-and-hold approach
- **Multi-timeframe Analysis**: Testing strategy effectiveness across different timeframes (5-min, 30-min, 1-hour, 2-hour, 12-hour)
- **Performance Metrics**: Calculating returns, annualized returns, and trade outcomes

## 📈 Strategy Description

The implemented trading strategy is based on the crossover between:
- 200-period Simple Moving Average (SMA)
- 20-period Exponential Moving Average (EMA)

### Trading Rules:
- **Buy Signal**: When the 20 EMA crosses above the 200 SMA
- **Sell Signal**: When the 20 EMA crosses below the 200 SMA
- **Take Profit**: 10 USD above entry price for long positions, 10 USD below entry price for short positions
- **Stop Loss**: 10 USD below entry price for long positions, 10 USD above entry price for short positions

## 🔍 Analysis Results

The backtesting results show that the moving average crossover strategy significantly outperformed the buy-and-hold approach:

### 1-Hour Timeframe (Recent 100 Days):
- **Buy and Hold Return**: -0.36%
- **Strategy Return**: 15.26%
- **Annualized Strategy Return**: 1.84%

### Historical Results (Since January 2022):
- The strategy demonstrated resilience during the 2022 cryptocurrency bear market
- Reduced maximum drawdown compared to buy-and-hold approach
- Generated consistent trading signals across multiple market conditions

## 🛠️ Technologies Used

- **Python**: Core programming language
- **Pandas/NumPy**: Data manipulation and analysis
- **Matplotlib**: Data visualization
- **Historic_Crypto API**: Accessing historical cryptocurrency data
- **Binance API**: Real-time and historical market data
- **Jupyter Notebook**: Interactive development and analysis

## 📝 Installation and Usage

1. Clone the repository
```bash
git clone https://github.com/yourusername/crypto-trading-strategy.git
cd crypto-trading-strategy
```

2. Install required dependencies
```bash
pip install -r requirements.txt
```

3. Set up API credentials
   - Create a `config.py` file for your Binance API credentials
   - Format: 
     ```python
     apiKey = 'your_binance_api_key'
     apiSecurity = 'your_binance_secret_key'
     ```

4. Run the Jupyter notebooks to analyze the strategies

## 🔮 Future Improvements

- Implement additional technical indicators (RSI, MACD, Bollinger Bands)
- Add machine learning models for predictive analysis
- Optimize take profit and stop loss levels dynamically
- Incorporate risk management techniques
- Create a real-time trading bot based on the strategy
- Analyze strategy performance across different cryptocurrencies
- Expand the 1-hour timeframe analysis which showed promising results (15.26% strategy return vs -0.36% buy-and-hold)

## 📊 Sample Visualizations

The repository includes various visualizations that help understand the trading strategy's performance:

### ETH Price with SMA and EMA Indicators
![ETH Price with SMA and EMA](eth_files/eth_11_0.png)

### Crossover Trading System with Buy/Sell Signals
![Crossover System with Signals](eth_files/eth_16_0.png)

### Multi-timeframe Analysis Results
![ETH 5-minute Timeframe](eth_files/eth_26_0.png)
![ETH 30-minute Timeframe](eth_files/eth_27_0.png)
![ETH 1-hour Timeframe](eth_files/eth_28_0.png)
![ETH 2-hour Timeframe](eth_files/eth_29_0.png)

## 📚 Resources and References

- [Historic_Crypto API Documentation](https://github.com/David-Woroniuk/Historic_Crypto)
- [Binance API Documentation](https://binance-docs.github.io/apidocs/)
- [Technical Analysis Fundamentals](https://www.investopedia.com/terms/t/technicalanalysis.asp)
- [Moving Average Strategies](https://www.investopedia.com/terms/m/movingaverage.asp)

---

*Disclaimer: This project is for educational and research purposes only. It is not financial advice, and you should not rely on this information for making investment decisions. Cryptocurrency trading involves significant risk of loss.*