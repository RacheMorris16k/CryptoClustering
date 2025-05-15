# CryptoClusterin

This project applies unsupervised machine learning techniques (K-Means Clustering and Principal Component Analysis) to group cryptocurrencies based on their price change behavior over various time periods.

---

## Dataset

- **File:** `crypto_market_data.csv`
- **Features:** Percentage price changes over 24h, 7d, 14d, 30d, 60d, 200d, and 1 year.
- **Target:** Discover natural groupings among cryptocurrencies using clustering.

---

## Tools Used

- Python
- pandas
- scikit-learn (`StandardScaler`, `KMeans`, `PCA`)
- hvPlot (for interactive visualizations)

---

##  Workflow Summary

### 1. **Data Preprocessing**
- Loaded and cleaned the dataset.
- Scaled features using `StandardScaler`.
- Set `coin_id` as index.

### 2. **K-Means Clustering (Original Scaled Data)**
- Applied elbow method for `k` values from 1 to 11.
- Plotted inertia to identify optimal `k`.
- ✅ **Best value of k: 4**

### 3. **Cluster Visualization**
- Clustered cryptocurrencies using the original scaled data.
- Plotted 24h vs 7d price change, colored by cluster.

### 4. **Dimensionality Reduction with PCA**
- Reduced features to 3 principal components.
- ✅ **Explained Variance: ~89.5%**
- Created new PCA-reduced DataFrame.

### 5. **K-Means Clustering (PCA Data)**
- Repeated elbow method on PCA data.
- ✅ **Best value of k: 4** (same as original)
- Plotted clusters using `PC1` vs `PC2`.

### 6. **Comparison and Analysis**
- Compared elbow curves (Original vs PCA).
- Compared clustering results visually.
- Answered reflection questions.

---

## 📌 Key Findings

- The elbow point occurred at **k = 4** for both original and PCA-reduced data.
- PCA reduced complexity while preserving **~90%** of the original variance.
- Clustering results were consistent, but PCA made the cluster structure easier to interpret visually.

---

## ✅ Requirements Met

- [x] Elbow method and visual selection of `k`
- [x] KMeans clustering with both original and PCA data
- [x] PCA transformation and explained variance analysis
- [x] Composite plots to compare clustering results
- [x] Markdown answers to reflection questions

---

## 📎 File Guide

- `Crypto_Clustering.ipynb`: Main notebook containing code and visualizations.
- `crypto_market_data.csv`: Input data file.
- `README.md`: This project summary.

---

-Rache Morris
-15/05/2025
