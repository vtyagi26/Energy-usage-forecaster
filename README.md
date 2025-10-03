# Energy Usage Forecaster Project

This text file contains all instructions and resources to set up and run the Energy Usage Forecaster project locally.

---

## 1. Project Overview

A regression and time series machine learning project that predicts daily or hourly household electricity consumption using historical energy usage, weather conditions, and temporal features. Demonstrates feature engineering, model comparison, and visualization techniques for practical forecasting.

---

## 2. Project Structure

```
energy-forecaster/
│── energy_forecaster.ipynb   # Jupyter notebook (main workflow)
│── energy.csv                # Sample/synthetic dataset
│── requirements.txt          # Python dependencies
│── README.md                 # Project documentation
```

---

## 3. Dataset

Columns:

* `date` (datetime)
* `temperature` (°C)
* `humidity` (%)
* `appliances` (number of active appliances)
* `usage` (target variable, kWh)

> Note: A sample synthetic dataset is included as `energy.csv`.

---

## 4. Installation Instructions

### Step 1: Clone the Repository

```
git clone https://github.com/YOUR_USERNAME/energy-usage-forecaster.git
cd energy-usage-forecaster
```

### Step 2: Create a Virtual Environment

```
python -m venv venv
# Windows
venv\Scripts\activate
# Linux/Mac
source venv/bin/activate
```

### Step 3: Install Dependencies

pip install -r requirements.txt

---

## 5. Running the Project

### Option 1: Jupyter Notebook

1. Open the notebook in VS Code or browser:

```bash
jupyter notebook energy_forecaster.ipynb
```

2. Run each cell sequentially to:

   * Load dataset
   * Perform feature engineering
   * Train Linear Regression, Random Forest, and XGBoost models
   * Evaluate performance
   * Visualize results

### Option 2: Python Script (Optional)

1. Export notebook as `.py` file.
2. Run in terminal:

python energy_forecaster.py
```
---

## 6. GitHub Instructions

### Initialize Repository Locally

git init
git remote add origin https://github.com/YOUR_USERNAME/energy-usage-forecaster.git
```

### Stage & Commit Files

```bash
git add .
git commit -m "Initial commit - Energy Usage Forecaster"
```

### Rename Branch (if needed)

git branch -M main
```

### Push to GitHub

git push -u origin main
```

---

## 7. README Overview

* **Project Description**: Predict household energy consumption.
* **Features**: Lag & seasonal feature engineering, model comparison, visualization.
* **Tech Stack**: Python, Pandas, Scikit-learn, XGBoost, Matplotlib.
* **Usage**: Jupyter notebook walkthrough.

---

## 8. Model Performance (Example)

| Model             | RMSE | MAE  |
| ----------------- | ---- | ---- |
| Linear Regression | 18.2 | 13.5 |
| Random Forest     | 12.8 | 9.7  |
| XGBoost           | 10.5 | 8.3  |

---

## 9. Future Enhancements

* Seasonal trend decomposition
* LSTM/GRU models for advanced sequential forecasting
* Multi-household datasets for large-scale prediction
* Deploy as a web app for real-time energy monitoring

---

## 10. License

MIT License

---

## 11. Synthetic Dataset Generator (Python Code)

import pandas as pd
import numpy as np

def generate_energy_dataset(start="2021-01-01", end="2021-12-31", freq="H", filename="energy.csv"):
    np.random.seed(42)
    date_range = pd.date_range(start=start, end=end, freq=freq)
    n = len(date_range)

    temperature = np.random.normal(20, 5, n)
    humidity = np.random.normal(50, 10, n)
    appliances = np.random.randint(1, 10, n)

    usage = (appliances * 2.5 + (25 - temperature) * 1.2 + np.random.normal(0, 2, n))

    df = pd.DataFrame({
        "date": date_range,
        "temperature": temperature,
        "humidity": humidity,
        "appliances": appliances,
        "usage": usage
    })

    df.to_csv(filename, index=False)
    print(f"Dataset generated: {filename} ({len(df)} rows)")
    return df

# Example usage
df = generate_energy_dataset()
```

---

# 12. Requirements.txt Example
```
pandas
numpy
scikit-learn
xgboost
matplotlib
seaborn
jupyter

---
```
