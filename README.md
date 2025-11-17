# Truck-sales_Time-Series-Class-Final-Project-
## 📝 Project Story — Truck Sales Time Series Forecasting

(Models used: ARIMA, SARIMA, SARIMAX, Prophet, LSTM)

This project focuses on forecasting truck sales using a variety of time-series models, ranging from traditional statistical approaches to modern deep-learning methods. The goal was to understand sales patterns, analyze long-term trends, and build models capable of predicting future truck sales to support business planning, budgeting, and inventory decisions.

---

## 🛠️ 1. Understanding the Problem & the Dataset

The project began with a simple but important business question:

**“How will truck sales behave in the future, and how can we forecast them accurately?”**

**To answer that, I loaded a dataset containing historical truck sales and examined:**

- Long-term sales trends

- Seasonal patterns (monthly/quarterly cycles)

- Potential outliers or abnormal periods

- Missing or inconsistent data

- Whether the dataset is stationary or requires differencing

This initial analysis guided which forecasting models would be most appropriate.

---

## 🔍 2. Exploratory Data Analysis (EDA)

**Using Python in a Jupyter/Colab Notebook, I performed a detailed time-series exploration:**

- Visualized the sales time series

- Investigated trend, seasonality, and cyclic behavior

- Checked autocorrelation and partial autocorrelation (ACF/PACF)

- Assessed data distribution, variance, and stationarity

- Identified potential structural changes or anomalies

The EDA stage helped reveal the underlying structure of the time series and prepared the direction for modeling.

---

## 🧼 3. Data Cleaning & Feature Engineering

**Before modeling, I cleaned and transformed the dataset to ensure accuracy:**

✔ Time Series Formatting

- Converted date column into proper datetime format

- Set the date as the time-series index

✔ Missing & Outlier Handling

- Filled or interpolated missing points

- Treated irregular spikes if needed

✔ Feature Engineering

**Created additional time-based features to support both statistical and deep-learning models:**

- Year

- Month

- Quarter

- Lag features (e.g., lag-1, lag-12)

- Moving averages (rolling windows)

These features assist models in recognizing patterns that aren’t immediately visible.

---

## 🤖 4. Forecasting Models Used

I implemented five forecasting approaches—each providing a different perspective on the data:

### 4.1) ARIMA Model

A classic statistical model for non-seasonal time series.

I experimented with different (p, d, q) values to find the best fit based on AIC and error scores.

### 4.2) SARIMA Model

An extension of ARIMA designed for seasonal data.

This model captures monthly or quarterly seasonal patterns using seasonal parameters (P, D, Q, s).

### 4.3) SARIMAX Model

A variation of SARIMA that supports external regressors (exogenous variables).

Even without many external features, SARIMAX helps benchmark performance and model stability.

### 4.4) Prophet Model

**Prophet is effective for data with:**

- strong seasonality

- trend changes

- weekly/monthly/yearly cycles

It also provides interpretable components: trend, seasonality, holiday effects.

### 5) LSTMs Model

A deep learning model designed specifically for sequential data.

**Steps included:**

- Scaling the data

- Reshaping into 3D tensors (samples, timesteps, features)

- Building LSTM layers followed by dense output

- Training and tuning the model

- Forecasting multiple steps ahead

LSTM excels at capturing non-linear and long-range dependencies in time series.

---

