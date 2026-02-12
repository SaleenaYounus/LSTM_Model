# 🌊 Groundwater Level Prediction Using LSTM

## 📌 Project Overview

This project applies a deep learning-based Vanilla  Long Short-Term Memory (LSTM) architecture to forecast seasonal groundwater levels (pre-monsoon and post-monsoon) across three districts in Kerala, India:

- Kollam  
- Pathanamthitta  
- Thiruvananthapuram  

Using 15 years of historical time-series data (2007–2022), the model demonstrates proof-of-concept seasonal forecasting using deep learning techniques.

---

## 📊 Dataset Description

- Sequential yearly groundwater level data
- Two well types:
  - Dug wells
  - Bore wells
- Separate datasets for:
  - Pre-monsoon
  - Post-monsoon
- Approximately 127 observations per locality
- Univariate time-series (single feature: yearly water level)

Missing Data:
- 2020 pre-monsoon excluded (COVID period)
- 2022 post-monsoon excluded (data unavailable)

---

## 🧠 Model Architecture

| Component | Value |
|-----------|--------|
| Framework | TensorFlow / Keras |
| Model Type | Vanilla LSTM |
| LSTM Units | 50 |
| Activation | ReLU |
| Loss Function | Mean Squared Error (MSE) |
| Optimizer | Adam |
| Epochs | 100 |
| Batch Size | 32 |

---

## 🔬 Methodology

1. Read groundwater data from Excel sheets.
2. Extract location-wise seasonal data.
3. Split dataset into training and testing sets.
4. Reshape input data to match LSTM input shape.
5. Train separate LSTM models for:
   - Pre-monsoon dataset
   - Post-monsoon dataset
6. Evaluate performance using Mean Squared Error (MSE).
7. Generate seasonal forecasts.

---

## 📈 Results

The LSTM model successfully captured seasonal groundwater trends across locations.

- Predicted values closely followed actual observed trends.
- Model performance was evaluated using Mean Squared Error (MSE).
- Visual comparison plots demonstrate good seasonal forecasting alignment.

(Example plots available in the notebook.)

---

## ⚠ Limitations

- Limited dataset size (15 yearly observations)
- Univariate time-series only
- No external climatic variables (e.g., rainfall, temperature)
- Equal train-test split may limit generalization

---

## 🚀 Future Improvements

- Walk-forward validation
- Multivariate modeling including climate variables
- Comparison with ARIMA and other statistical models
- Hyperparameter optimization

---

## 🛠 Tech Stack

- Python
- Pandas
- NumPy
- TensorFlow / Keras
- Matplotlib

---

## 📂 Repository Contents

- `LSTM_Model.ipynb` – Main model implementation notebook
- `README.md` – Project documentation

---

## 📚 References

- Hochreiter, S., & Schmidhuber, J. (1997). Long Short-Term Memory.
- Colah’s Blog: Understanding LSTMs

