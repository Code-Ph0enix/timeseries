# 📈 Tesla Stock Forecasting using VoI (Value of Information)

This project investigates and compares statistical time-series models for forecasting **Tesla (TSLA) stock prices**, with a specific focus on the **Value of Information (VoI)** framework. It evaluates models based on how effectively additional data or external variables improve predictive accuracy, using VoI as a metric for decision-making.

---

## 📚 Background

The stock market is influenced by many dynamic factors, making accurate price forecasting both difficult and essential. In this project, we compare three forecasting models:

- **VAR (Vector AutoRegression)**
- **ARIMA (AutoRegressive Integrated Moving Average)**
- **SARIMAX (Seasonal ARIMA with exogenous variables)**

We apply the **Value of Information** methodology described in the research paper *"Value of Information in the Mean-Square Case and its Application to the Analysis of Financial Time-Series Forecast"* by Roman V. Belavkin et al., to assess which model delivers the most value when additional information (like volume) is introduced.

---

## 🎯 Objective

- To evaluate and compare forecasting models based on **VoI** rather than just RMSE
- To quantify how much **additional information** improves prediction performance
- To identify the most effective model for **daily stock price prediction of Tesla (TSLA)**

---

## 🔍 Methodology Overview

We calculate **Value of Information (VoI)** as:

> VoI = RMSE(Model A) - RMSE(Model B with added variable)

This tells us how valuable the **additional data** (like trading volume) is to a model’s predictive power.

### 🧠 Key Concepts Applied:
- Shannon’s Entropy  
- Conditional Entropy  
- Mutual Information  
- VoI Expression  
- Cost-Benefit Analysis

---

## 📊 Dataset

- **Name:** `TSLA.csv`
- **Source:** [Kaggle Dataset](https://www.kaggle.com/datasets/varpit94/tesla-stock-data-updated-till-28jun2021)
- **Columns:** Date, Open, High, Low, Close, Adj Close, Volume  
- **Range:** June 29, 2010 – March 24, 2022

---

## 🛠️ Models Compared

| Model   | Description |
|---------|-------------|
| **VAR**     | Captures linear interdependencies among multiple time series. Best when variables are interrelated. |
| **ARIMA**   | Traditional univariate time-series model. Works well for non-seasonal series. |
| **SARIMAX** | Enhances ARIMA by supporting seasonal data and external regressors like trading volume. |

---

## 📈 Implementation & Results

We evaluated several model combinations:

1. **SARIMAX vs VAR**
2. **SARIMAX + Volume vs VAR**
3. **ARIMA + Volume vs VAR**

The analysis showed:

- **ARIMA** had the **highest VoI** when used to predict Tesla's daily closing prices.
- **VAR and ARIMA** performed better than **SARIMAX**, likely due to the lack of seasonality in the dataset.

---

## ✅ Conclusion

The ARIMA model outperforms others in terms of **Value of Information**, particularly when used with relevant auxiliary data like **trading volume**. SARIMAX, though powerful for seasonal data, was less effective here due to the non-seasonal nature of Tesla’s stock behavior.

---

## 🔗 References & Resources

- [Original VoI Research Paper (Belavkin)](https://arxiv.org/abs/2410.01831)  
- [Kaggle Dataset – Tesla Stock](https://www.kaggle.com/datasets/varpit94/tesla-stock-data-updated-till-28jun2021)  
- [ARIMA, SARIMA, SARIMAX Explained – ZTM Blog](https://zerotomastery.io/blog/arima-sarima-sarimax-explained/)  
- [Wikipedia – Vector AutoRegression](https://en.wikipedia.org/wiki/Vector_autoregression)  
- [Presentation Video (YouTube)](https://youtu.be/GPsXWkLmy3k)
 
