# RegimeRadar — Week 2: Feature Engineering (depth20 + aggTrade)

Welcome to Week 2 of RegimeRadar!  
In this week, we'll transform raw order book data into meaningful features for regime detection.

---

## 📊 Data Sources

- `depth20.csv` → Top 20 levels of bid/ask prices & volumes (order book snapshots)
- `aggTrade.csv` → Aggregated tradebook data (executed trades)

---

## 🎯 Goals

- Extract financial features from depth20 data
- Compute key indicators for liquidity, volatility, and order book imbalance
- Generate normalized features for clustering models in Week 3

---

## 🔧 Tasks

### ✅ Load and inspect data
- Use pandas to load depth20 & aggTrade

### ✅ Feature Engineering
- Spread = Ask Price (Level 1) - Bid Price (Level 1)
- Mid-Price = (Ask + Bid) / 2
- Order Book Imbalance (Level 1)
- Full Depth Order Book Imbalance (20 levels)
- Rolling Volatility (using Mid-Price)
- (Optional) Tradebook features from aggTrade

### ✅ Visualizations
- Plot Spread, Mid-Price, OBI, Rolling Volatility over time

### ✅ Export final feature dataset for Week 3

---

## 📈 Deliverables

- Jupyter Notebook with:
  - Cleaned data
  - Engineered features
  - 4 visualizations
  - Exported feature CSV file
