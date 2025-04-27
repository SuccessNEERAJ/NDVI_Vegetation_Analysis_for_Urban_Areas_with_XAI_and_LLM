# NDVI Vegetation Analysis and Prediction for Urban Areas using Satellite Images with XAI and LLM Integration

## 📚 Project Overview

This research focuses on forecasting the **Normalized Difference Vegetation Index (NDVI)** values for urban areas using **Random Forest** and **Long Short-Term Memory (LSTM)** models. 
It also integrates **Explainable AI (XAI)** techniques (SHAP values) and a **Large Language Model (LLM)** powered by the **Groq API** to make the model outputs understandable for non-technical users.

> 📢 **Note**: This research has been presented, and the paper has been accepted for publication. The final publishing process is currently ongoing with **CRC Press**.

The project aims to assist in **agricultural decision-making**, **drought surveillance**, and **climate change research** by providing easy-to-interpret vegetation insights.

---

## 🔬 Research Highlights

- **Models Used**: 
  - Random Forest Regressor (Best Performer)
  - Long Short-Term Memory (LSTM)

- **Explainability**: 
  - SHAP Values used to identify important features.

- **LLM Integration**: 
  - Groq API + Llama LLM for an interactive, plain-language Q&A dashboard.

- **Use Cases**:
  - Improved crop management.
  - Drought monitoring.
  - Precision farming.

---

## 🗃️ Dataset Details

- **Source**:
  - Sentinel-2 Satellite Imagery (via Google Earth Engine)
  - Climate and soil data (via Open-Meteo Weather API)

- **Location**: Ludhiana, Punjab, India (30.89°N, 75.95°E)

- **Data Timeline**: 2019 to 2025 (weekly NDVI values)

- **Key Features**:
  - NDVI mean, soil moisture, soil temperature
  - Climate metrics: temperature, precipitation
  - Derived features: lag features, rolling averages, seasonal indicators

---

## 🛠️ Methodology

1. **Data Collection**:  
   - Downloaded weekly Sentinel-2 images, calculated NDVI, merged with climate and soil data.
   
2. **Data Preprocessing**:  
   - Handling missing values, scaling, feature engineering (lags, moving averages).

3. **Model Training**:
   - Trained Random Forest and LSTM models.
   - Hyperparameter tuning using `RandomizedSearchCV` and `TimeSeriesSplit`.
   - Evaluated using RMSE, MAE, and R² scores.

4. **Model Explainability**:
   - Used SHAP to understand key features influencing NDVI prediction.

5. **LLM Dashboard**:
   - Built an interactive dashboard using Streamlit.
   - JSON summaries of NDVI, climate, and soil data fed to Llama LLM via Groq API.

---

## 📈 Results

| Model | Validation RMSE | Test RMSE | R² Score |
|:-----:|:---------------:|:---------:|:--------:|
| Random Forest (Final Tuned) | 0.0267 | 0.0542 | 0.6936 |
| LSTM | 0.0731 | 0.0505 | - |

- **Random Forest** outperformed LSTM after hyperparameter optimization.
- **Top Features (SHAP Analysis)**: 
  - 4-week moving average NDVI
  - 1-week lag NDVI
  - Soil moisture (0-7 cm depth)
  - Temperature features

---

## 🖥️ Dashboard Demo

- **Ask Questions** about NDVI trends, crop suggestions, soil conditions.
- **Powered by** Groq API and Llama LLM.
- **Built with** Streamlit for real-time interaction.

---