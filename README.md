# Energy Usage Forecaster ⚡

A regression and time series machine learning project that predicts **daily or hourly household electricity consumption** using historical energy usage, weather conditions, and temporal features. This project demonstrates feature engineering, model comparison, and visualization techniques for practical forecasting.

---

## Table of Contents
- [Project Overview](#project-overview)
- [Features](#features)
- [Dataset](#dataset)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Model Performance](#model-performance)
- [Future Work](#future-work)
- [License](#license)

---

## Project Overview
Accurate energy consumption forecasting helps households and energy providers optimize usage, reduce costs, and implement energy-saving strategies. This project explores different regression models and evaluates their performance in predicting energy usage.

---

## Features
- **Time Series Feature Engineering:** Created lag features (previous usage values), temporal features (hour, day of week, month), and seasonal indicators.
- **Model Comparison:** Implemented **Linear Regression**, **Random Forest Regressor**, and **XGBoost Regressor**.
- **Evaluation Metrics:** Used **RMSE** and **MAE** to measure model performance.
- **Visualization:** Plotted actual vs predicted consumption and visualized feature importance.
- **Modular Code:** Easy-to-extend structure for new datasets or models.

---

## Dataset
- Simulated or real-world household energy consumption dataset.
- Columns include:
  - `date` (datetime)
  - `temperature` (°C)
  - `humidity` (%)
  - `appliances` (number of active appliances)
  - `usage` (target variable, kWh)

> Note: A sample **synthetic dataset** is included (`energy.csv`) for testing purposes.

---

## Tech Stack
- **Python** for programming
- **Pandas & NumPy** for data manipulation
- **Scikit-learn** for Linear Regression and Random Forest
- **XGBoost** for gradient boosting regression
- **Matplotlib & Seaborn** for visualization
- **Jupyter Notebook** for interactive workflow

---

## Installation
1. Clone the repository:
```bash
git clone https://github.com/YOUR_USERNAME/energy-usage-forecaster.git
cd energy-usage-forecaster
