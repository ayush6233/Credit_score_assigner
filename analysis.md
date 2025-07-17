Analysis of DeFi Credit Scoring Pipeline

1. Objective

Compute risk‑adjusted credit scores for Aave v2 users by detecting anomalous on‑chain behavior.

2. Data Ingestion

Input: JSON array of wallet transactions

Fields: wallet address, timestamp, asset, amount, transaction type

3. Feature Engineering

Transaction count: total, deposits, borrows, repayments

Volume metrics: total volume per asset

Time‑based stats: average inter‑transaction interval, recency

Activity diversity: number of unique assets, actions

4. Modeling Approach

Isolation Forest: unsupervised anomaly detection

contamination: proportion of wallets expected as outliers

n_estimators: number of trees for robustness

Scores mapped 0–1000: lower score ⇒ more anomalous

5. Results & Validation

Histograms of score distribution to verify separation of normal vs. abnormal

Spot‑check known wallets to ensure reasonable ranges

