

## 🎯 Your Mission

Your goal is to build a **Market Regime Detection system** using unsupervised clustering. You'll start with raw order book and trade data and extract meaningful signals that reflect **market "moods"** — volatile, stable, bullish, bearish, etc.

Use what we’ve already explored — but think *yourself* about what signals matter.

---

### 📌 Step-by-Step Breakdown

#### 1. **Data Cleaning & Resampling**
- Load the trade and order book data (`trade_df`, `depth_df`)
- Clean timestamp columns and convert them to datetime
- Resample both datasets to **1-second intervals** to align time points
- Make sure trade and depth are **merged correctly on time**

✅ Output: A merged dataframe (`merged_df`) with 1s-aligned trade and depth stats

---

#### 2. **Feature Engineering**
Create a new dataframe `features` using the merged data:
- Statistical features: `price_var`, `avg_time_diff`, `value_per_second`
- Volatility features: rolling std of log returns over 10s, 30s
- VWAP & VWAP Shift: calculate rolling VWAP and its change over 10s/30s
- OBI (Order Book Imbalance): compute average imbalance at 5, 10, and 20 levels
- Market stats: average buy/sell price and volume over 1s buckets
- Squared log return per second and its variance

✅ Output: `features_with_OBI_market.csv` saved to Drive or GitHub

---

#### 3. **Clustering & Visualization**
- Select relevant features (you decide what’s meaningful)
- Standardize the data using `StandardScaler`
- Use **Elbow method** to choose `k` (number of clusters)
- Apply **KMeans clustering** on the scaled data
- Reduce the features to 2D using **PCA** and plot the clusters

---

#### 4. **Cluster Interpretation**
- Label each cluster (based on average volatility, volume, price movement, OBI)
- Plot a **heatmap** showing feature averages per cluster
- Try to name each cluster:
  - “High Volatility Bullish”
  - “Stable Neutral”
  - “Low Volume Bearish”

You’re trying to reverse-engineer market behavior using ML.

---

## 📦 What to Submit

| File | Description |
|------|-------------|
| `features_with_OBI_market.csv` | Your final feature set |
| `RegimeRadar_Final.ipynb` or `.py` | Clean, step-by-step notebook |
| `elbow_plot.png` | Elbow method to choose `k` |
| `pca_clusters.png` | 2D cluster visualization |
| `cluster_heatmap.png` | Heatmap of cluster-wise stats |
| `README.md` | Write: What features you picked, how you clustered, what you learned |

---

## 💡 Optional (Extra Points)
- Try `HDBSCAN` instead of KMeans and compare results
- Visualize regime *transitions* over time
- Plot cluster frequency (how many seconds the market stayed in each regime)


---

> 🎓 Remember: this is a *real-world pipeline* — clean raw data, extract smart features, find structure, and interpret it.

