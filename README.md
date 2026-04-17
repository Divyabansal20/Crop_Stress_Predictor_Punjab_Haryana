# 🌾 Crop Stress Prediction using Hybrid Time-Series Modeling

## 📌 Problem Context

Agricultural decision-making often relies on fragmented and noisy data from multiple sources such as satellite imagery, weather records, and soil conditions.
This project addresses the challenge of predicting **crop stress (via NDVI trends)** under real-world constraints like incomplete data, temporal dependencies, and seasonal variability.

---

## 🎯 Objective

To build a robust time-series prediction pipeline that accurately forecasts NDVI values and captures both:

* Seasonal trends (long-term patterns)
* Non-linear fluctuations (short-term stress signals)

---

## 🧠 Methodology

### 🔹 Data Integration

* Satellite Data → NDVI (vegetation health)
* Weather Data → Temperature, Rainfall
* Soil Data → Supporting environmental features

Handled missing values, inconsistencies, and aligned multi-source datasets across a **3-year timeline**.

---

### 🔹 Feature Engineering

Designed domain-specific features to improve prediction quality:

* **Heatwave Index** → Captures extreme temperature stress
* **Rainfall Aggregation** → Reflects water availability
* **Lag Variables** → Models temporal dependencies
* **Seasonal Signals** → Encodes crop cycles

---

### 🔹 Modeling Approach

Implemented a **hybrid modeling strategy**:

#### 📈 SARIMAX (Statistical Model)

* Captures seasonality and long-term trends
* Effective for structured temporal patterns

#### ⚡ XGBoost (Machine Learning Model)

* Captures non-linear relationships
* Handles complex feature interactions

---

### 🔹 Model Comparison

| Model   | Strength                       | Limitation                    |
| ------- | ------------------------------ | ----------------------------- |
| SARIMAX | Strong seasonal trend modeling | Limited non-linear capability |
| XGBoost | Captures complex patterns      | Weak temporal structure       |

👉 Final insight:
A **hybrid perspective** provides better robustness than relying on a single model.

---

## 📊 Results & Insights

* Successfully modeled NDVI trends across **3 years of agricultural data**
* Observed that:

  * SARIMAX performs well in stable seasonal phases
  * XGBoost performs better during irregular stress conditions
* Feature engineering significantly improved prediction stability

---

## ⚙️ Tech Stack

* Python
* Pandas, NumPy
* Matplotlib
* Scikit-learn
* XGBoost
* Statsmodels (SARIMAX)

---


## 💡 Key Learnings

* Handling ambiguous and incomplete real-world datasets
* Time-series forecasting with both statistical and ML approaches
* Importance of domain-driven feature engineering
* Trade-offs between interpretability and performance

---

## 🚀 Future Improvements

* Build an interactive dashboard using Streamlit
* Deploy model as an API for real-time predictions
* Experiment with deep learning models (LSTM, Transformers)
* Integrate real-time satellite data pipelines
