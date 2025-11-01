# 🌦️ Weather Forecasting using MA, SARIMAX & LSTM

This project forecasts temperature for **Delhi (1996–2017)** using **classical time series models** and a **deep learning model**.

Models used:

* ✅ **MA (Moving Average)** — baseline smoothing model for short-term forecasting
* ✅ **SARIMAX** — seasonal ARIMA with exogenous capability for monthly forecasting
* ✅ **LSTM Neural Network** — used at the end to capture long-term temporal patterns

---

## 🎯 Project Objective

To forecast temperatures effectively by comparing:

* Classical statistical models (MA & SARIMAX)
* Deep Learning (LSTM)

---

## 📊 Dataset

* **Location:** Delhi, India
* **Frequency:** Hourly data (1996–2017)
* **Target Variable:** Temperature (°C)

Resampling done for:

| Frequency       | Purpose                                 |
| --------------- | --------------------------------------- |
| Hourly          | Raw data source                         |
| Daily Average   | Smoother trends, used with MA model     |
| Monthly Average | Seasonal forecasting, used with SARIMAX |

---

## 🧪 Methodology

### ✅ Exploratory Data Analysis (EDA)

* Hourly → Daily → Monthly trend visualization
* Seasonality patterns
* Trend & yearly variations

### ✅ Stationarity Check

* Augmented Dickey-Fuller test
* Differencing applied to achieve stationarity

### ✅ Models Applied

| Model                   | Purpose                                      |
| ----------------------- | -------------------------------------------- |
| **MA (Moving Average)** | Simple baseline for daily prediction         |
| **SARIMAX**             | Handles trend + seasonality for monthly data |
| **LSTM**                | Captures complex long-term time dependencies |

### ✅ Model Training Steps

* Train-test split
* For LSTM:

  * Data normalization
  * Sliding window sequence creation
  * Neural network training

---

## 📈 Evaluation

* **Metric:** RMSE (Root Mean Squared Error)
* Plots for:

  * Actual vs Predicted values
  * Forecast visualization
  * Loss curve for LSTM

> SARIMAX handled seasonal structure well, while LSTM improved long-term modeling.

---

## 🧠 Key Learnings

* Importance of resampling (hourly → daily → monthly)
* Stationarity is critical for ARIMA-based models
* SARIMAX handles seasonality better than simple MA
* LSTM effectively learns non-linear temporal patterns

---

## 🚀 Future Work

* Add humidity, pressure, wind as features in SARIMAX & LSTM
* Compare with **Prophet / XGBoost** for time-series
* Deploy via **Streamlit** with real-time updates
* Tune LSTM architecture further (more layers, GRU comparison)

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Statsmodels
* TensorFlow / Keras
* Matplotlib / Seaborn
* Jupyter Notebook

## 📁 Notebook Contains

* Data exploration & cleaning
* Resampling (hourly → daily → monthly)
* Stationarity testing & differencing
* MA & SARIMAX modeling
* LSTM modeling
* Evaluation & visualization
