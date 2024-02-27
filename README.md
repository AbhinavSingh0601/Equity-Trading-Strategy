# FINCLUB Open Project on Technical Analysis

## Technical Analysis of MACD Strategy for DJI, TSLA, and MSFT Stocks

### Introduction
Technical analysis is a popular approach in financial markets that involves analyzing historical price and volume data to make informed trading decisions. One of the key indicators used in technical analysis is the Moving Average Convergence Divergence (MACD) indicator, which helps identify potential buy and sell signals in a stock's price chart. In this project, we have implemented a MACD strategy to analyze the performance of three different stocks: Dow Jones Industrial Average (DJI), Tesla Inc. (TSLA), and Microsoft Corporation (MSFT).

The MACD strategy is based on the intersection of the MACD line and the Signal (SIG) line, along with specific volume conditions. This strategy provides buy (go long) and sell (go short) signals for a particular stock. However, it is important to note that the buy/sell orders are only executed when the trading volume for the stock exceeds the average volume over the previous 10 days. If the volume conditions are not met, the intersection results in a square-off position, where no trade is executed.

The strategy relies on the variable "position" to determine the current trading status. When "position" is set to 1, it indicates a long position, -1 represents a short position, and 0 means no position is currently held or closed position to be held.

### Formulas for Calculating Results
Before delving into the results for DJI, TSLA, and MSFT stocks, let's understand the formulas used to calculate the key performance metrics:

1. **Sharpe Ratio:**
   - Sharpe Ratio of Actual Returns = (Mean of Actual Returns - Risk-Free Rate) / Standard Deviation of Actual Returns
   - Sharpe Ratio of Daily Returns = (Mean of Daily Returns - Risk-Free Rate) / Standard Deviation of Daily Returns

2. **Annualized Return:**
   - Annualized Return = ((Final Booksize / Initial Booksize) ^ (1 / Number of Years)) - 1

3. **Benchmark Return:**
   - Benchmark Return is a predefined benchmark return used for comparison (e.g., 2.63% annually).

4. **Number of Executed Trades:**
   - Count of executed buy and sell trades over the backtesting period.

5. **Maximum Drawdown:**
   - Maximum Drawdown = (Lowest Point - Highest Point) / Highest Point

6. **Win Ratio:**
   - Win Ratio = (Number of Positive Returns) / (Total Number of Trades)

7. **Loss-Making Trades:**
   - Count of trades with negative returns.

8. **Profit-Making Trades:**
   - Count of trades with positive returns.

9. **Largest Loss-Making Trade:**
   - The largest percentage loss among all trades.

10. **Largest Profit-Making Trade:**
    - The largest percentage profit among all trades.

### Results
Now, let's dive into the results for DJI, TSLA, and MSFT stocks based on the MACD strategy:

#### Dow Jones Industrial Average (DJI):
- Sharpe Ratio of Actual Returns: 0.0383
- Sharpe Ratio of Daily Returns: 0.0344
- Annualized Return: 2.63%
- Benchmark Return: 2.63%
- Number of Executed Trades: 100
- Maximum Drawdown: -18.30%
- Win Ratio: 0.53
- Loss-Making Trades: 47
- Profit-Making Trades: 53
- Largest Loss-Making Trade: -4.96%
- Largest Profit-Making Trade: 3.15%
- Final Booksize: $11,387.25

#### Tesla Inc. (TSLA):
- Sharpe Ratio of Actual Returns: 0.1207
- Sharpe Ratio of Daily Returns: 0.0628
- Annualized Return: 114.37%
- Benchmark Return: 2.63%
- Number of Executed Trades: 582
- Maximum Drawdown: -97.90%
- Win Ratio: 0.5670
- Loss-Making Trades: 252
- Profit-Making Trades: 330
- Largest Loss-Making Trade: -17.18%
- Largest Profit-Making Trade: 21.06%
- Final Booksize: $452,661.29

#### Microsoft Corporation (MSFT):
- Sharpe Ratio of Actual Returns: 0.0802
- Sharpe Ratio of Daily Returns: 0.0527
- Annualized Return: 32.06%
- Benchmark Return: 2.63%
- Number of Executed Trades: 623
- Maximum Drawdown: -75.50%
- Win Ratio: 0.5684
- Loss-Making Trades: 268
- Profit-Making Trades: 353
- Largest Loss-Making Trade: -14.22%
- Largest Profit-Making Trade: 14.74%
- Final Booksize: $40,166.46

### Insights and Strategy Development
The results of the MACD strategy for DJI, TSLA, and MSFT stocks provide valuable insights into the performance and risk associated with this particular trading approach. Here are some key takeaways and considerations for further strategy development:

1. **High Variability in Results:** The strategy's performance varies significantly across the three stocks. TSLA exhibited the highest annualized return, but it also had the largest maximum drawdown. DJI had a more conservative performance, with a lower annualized return and a smaller drawdown. MSFT struck a balance between the two.

2. **Risk Management:** The high maximum drawdown in the TSLA strategy suggests that risk management is crucial. Further development of the strategy could include mechanisms to limit losses during adverse market conditions.

3. **Benchmark Comparison:** The choice of benchmark significantly impacts strategy evaluation. Consider using a benchmark that closely represents the asset class or market you are trading in for a more meaningful comparison.

4. **Portfolio Diversification:** Diversifying the portfolio by including multiple assets can help spread risk. Analyze how the strategy performs in a diversified portfolio context.

5. **Market Conditions:** The strategy's performance can be influenced by market conditions and economic events. Periodic monitoring and adaptation to changing conditions are essential.

### Improvements for the MACD Strategy
Here are three key improvements to consider for the MACD trading strategy:

1. **Advanced Risk Management:** Enhance risk management by implementing dynamic stop-loss and take-profit levels based on factors like historical volatility and recent price movements.

2. **Machine Learning Integration:** Consider incorporating machine learning models to improve signal accuracy and enhance the strategy's precision.

3. **Multi-Asset Analysis:** Extend the strategy to analyze and trade multiple assets simultaneously for better diversification and risk management.

### Python Files and How to Run the MACD Indicator
In this section, we will describe the three Python files involved in this project and provide instructions on how to run the MACD indicator for your own analysis.

1. **Main.py:** Core script for gathering financial data, calculating MACD and trading signals, and visualizing the results using the yfinance library. Follow the instructions provided to install the required libraries and run the script.

2. **Results.py:** Responsible for calculating key performance metrics and portfolio

 returns based on trading signals. It is automatically imported and executed within Main.py.

3. **Plotting.py:** Used to create visual representations of the results. It is called from Main.py to create relevant plots.

#### Instructions for Running the MACD Indicator:
1. Ensure Python is installed on your system.
2. Install required libraries (yfinance and matplotlib) using pip.
3. Download or create Main.py, Results.py, and Plotting.py files in the same directory.
4. Open a terminal or command prompt, navigate to the directory, and run Main.py using the provided command.
5. The script will fetch historical stock data, calculate MACD and trading signals, and display the plots of buy and sell signals on the stock's price chart.

#### Notes:
- Ensure an internet connection to fetch data from Yahoo Finance using yfinance.
- Install required libraries and dependencies correctly to avoid errors.

By following these instructions, you can run the MACD indicator and analyze the results for different stocks. The provided Python files automate the process for convenient evaluation of the MACD trading strategy.
