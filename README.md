 # 📊 Crypto-Sentiment-Trading-Analysis


This project explores the relationship between **Bitcoin market sentiment** (based on the Fear & Greed Index) and **real-world trader performance** from the Hyperliquid trading platform. It includes data analysis, visualizations, and a machine learning model to predict trade profitability based on market sentiment and trade-related features.

---

## 🔍 Problem Statement

> Can market sentiment indicators (like "Fear" and "Greed") help predict whether a crypto trade will be profitable?

---

## 📁 Dataset Information

### 🗂 1. Fear & Greed Index
- Columns: `date`, `value`, `sentiment`
- Simulated sentiment was used because original data did not cover the recent time window of trader data.

### 🗂 2. Hyperliquid Trader Data
- Columns: `Account`, `Symbol`, `Execution Price`, `Size Tokens`, `Side`, `Timestamp`, `Closed PnL`, etc.
- Timestamp in milliseconds was parsed to generate `date`.

---

## 🔧 Tools Used
- **Python**
- **Pandas**, **NumPy**
- **Matplotlib**, **Seaborn**
- **Scikit-learn** (for ML modeling)

---

## 📊 Exploratory Data Analysis

- Bar plot: Average Closed PnL grouped by sentiment (Fear, Greed, etc.)
- Buy ratio distribution by sentiment group
- Correlation matrix between sentiment and Closed PnL

---

## 🧠 Machine Learning Model

- Model: `RandomForestClassifier`
- Features used:
  - `sentiment_score` (encoded from sentiment)
  - `Execution Price`
  - `Size Tokens`
  - `Trade Side` (buy/sell encoded)
- **Class balancing** was performed to fix the model bias toward loss-making trades.

### 🔎 Results:
- **Accuracy**: 77%
- **F1-Score**: 0.77
- Both profit and loss trades are now correctly classified.
  
---

## 📌 Key Insights

- Market sentiment alone shows very weak correlation with profit (r ≈ 0.004).
- Adding trade-specific features improves prediction significantly.
- Traders show slightly higher profit during periods of "Greed".
- Buy vs. sell ratios remain fairly balanced across sentiment groups.

---

## 🧪 How to Run

1. Clone the repo:
   ```bash
   [git clone https://github.com/your-username/Crypto-Sentiment-Trading-Analysis.git](https://github.com/hitesh-bhatnagar/Crypto-Sentiment-Trading-Analysis.git)
   cd Crypto-Sentiment-Trading-Analysis
