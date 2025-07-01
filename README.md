# decentralized-portfolio-optimizer

A high‑frequency crypto portfolio toolkit that fuses GRU one‑hour price forecasts with Dirichlet‑sampling Sharpe optimization. This repository powers the research pipeline—from raw data ingestion to three‑theory regime analysis—via a single Jupyter notebook.

## Notebook Structure

1. **Individual Data Extraction & Processing**  
   Fetch and clean hourly OHLCV from Binance.  
2. **PCA‑Based Indexing**  
   Build a composite DAO index via principal component analysis.  
3. **Model Training & Evaluation**  
   Load or re‑run data preprocessing, then train asset‑specific GRUs.  
4. **Forecasting**  
   Generate one‑hour‑ahead price predictions for all assets.  
5. **Optimization**  
   Apply Dirichlet‑sampling to maximize forecast‑driven Sharpe ratios.  
6. **DAO Allocation & Sharpe Progression**  
   Plot optimal DAO weights and Sharpe trajectories over time.  
7. **DAO Allocation & Sharpe Correlation**  
   Compute correlation between DAO weight and Sharpe ratio.  
8. **DAO Allocation & Volatility Correlation**  
   Analyze DAO weight vs. portfolio standard deviation.  
9. **Market Regime Analysis**  
   Segment results into bull, bear, and neutral regimes; apply Markowitz, Drawdown‑Shock, and Beta‑Score lenses.

## Notes

- **Model Training Shortcut**: The **Model Training & Evaluation** cell includes its own data‑loading and preprocessing steps. If you’ve already doesnt intend to index an group of assets, directly run the **Model Training & Evaluation**. It will ask you to either use already available file or extract new data from the API.
- **Expected Errors**: You may encounter warnings or memory errors on large datasets. Ensure your API credentials are valid, you have sufficient RAM, and consider breaking data into smaller segments.
