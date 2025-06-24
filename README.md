# 1.Project Overview

This project develops and tests a weekly calendar-spread arbitrage strategy for the CSI 500 stock index futures market. The strategy aims to identify profitable cross-period combinations of futures contracts, improve portfolio returns, and reduce risk through effective hedging.
We use machine learning (Random Forest, Neural Networks) to predict 5-day annualized returns on six cross-period combinations, guiding weekly rebalancing decisions for arbitrage trading.

# 2.Dataset
- **Source**: Wind Financial Terminal (China's equivalent of Bloomberg)
- **Period**: April 2015 – June 2023
- **Size**: ~80,000 records

- **Data fields**:
Futures contract prices, volumes, open interest
Stock index data (CSI 500, CSI 300, SSE 50, CSI 1000, Wind All-A)
Fund NAVs (index-enhanced, neutral strategy funds)
Broker position data (top 5, 10, 20 brokers)

# 3.Tools & Technologies
Python (pandas, NumPy, matplotlib, seaborn)
scikit-learn, statsmodels (for feature engineering, model training)
Wind API + Excel (data acquisition and integration)

# 4.Methods
Data cleaning & transformation: Handle missing data via forward/backward fill; derive features (risk-return, hedging demand, basis, trading structure)
Dimensionality reduction: Feature selection + PCA
Modeling: Random Forest, Neural Network models for return prediction
Evaluation: Compare MSE, success rate (whether predicted combination outperforms median of all combinations)
Backtesting: Apply model-selected strategies on out-of-sample data, assess Sharpe ratio, drawdown

# 4.Key Findings
The model predicts calendar-spread returns with a success rate exceeding 55%.
Random Forest showed stronger stability and interpretability compared to Neural Networks in backtesting.
The strategy achieved annualized returns exceeding median market performance, with Sharpe ratios above 1 in stable periods.

# 6. Business Impact
Helps institutional investors manage risk and improve capital efficiency in volatile markets.
Provides a framework for systematic weekly arbitrage decisions in China’s stock index futures market.
