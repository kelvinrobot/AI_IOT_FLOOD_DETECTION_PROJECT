
 AI Real-time IoT Flood Detection System

This project is an intelligent, real-time flood detection backend powered by sensor data and AI. It supports model fusion of LSTM, CatBoost, XGBoost, and Autoencoder for robust flood prediction.

##  Features

-  Receives real-time environmental data from IoT sensors
-  Uses 4 powerful AI models (CatBoost, XGBoost, LSTM, Autoencoder)
-  Smart fusion logic for accurate flood risk prediction
-  Returns flood probability, severity class, and risk score (all as percentages)
-  Upload new CSVs to retrain all models on-the-fly
- ⚙ Built with FastAPI (fully production-ready)

##  Models

| Model         | Purpose               |
|---------------|------------------------|
| CatBoost      | Binary flood prediction |
| XGBoost       | Regression for risk score |
| LSTM          | Time-series flood detection |
| Autoencoder   | Anomaly detection on environment |

##  API Endpoints

###  `POST /predict`

Send real-time sensor readings to get prediction.

**Example JSON:**

```json
{
  "avg_temp": 28.4,
  "humidity": 76.6,
  "precip": 0.0,
  "windspeed": 16.6,
  "sealevelpressure": 1009.6,
  "cloudcover": 36.6,
  "solarradiation": 241.3,
  "flood_lag_1": 0,
  "flood_lag_2": 0,
  "flood_lag_3": 0,
  "flood_lag_4": 0,
  "flood_lag_5": 0,
  "smi_linear_norm": 0.39,
  "month": 10
}

