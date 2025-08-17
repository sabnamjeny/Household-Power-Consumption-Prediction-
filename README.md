# ⚡ PowerPulse: Household Energy Usage Forecasting

## 📌 Overview
PowerPulse is a Data Science project that predicts **household electricity consumption** using historical data.  
The goal is to help in **energy management, demand forecasting, and better decision-making** for smart grids.  

This project applies **Machine Learning (Neural Networks)** to forecast energy usage and analyze key patterns in power consumption.

---

## 📂 Dataset
- **Source:** [Individual Household Electric Power Consumption Dataset](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)  
- **Time Period:** Dec 2006 – Nov 2010  
- **Observations:** ~2,075,259 rows (1-min sampling rate)  
- **Features:**
  - Date, Time  
  - Global Active Power (kW)  
  - Global Reactive Power (kW)  
  - Voltage (V)  
  - Global Intensity (A)  
  - Sub-metering (1, 2, 3)  
  - Derived features: Year, Month, Day, Hour, DayOfWeek  

---

## ⚙️ Steps & Workflow
1. **Data Preprocessing**
   - Missing values handled  
   - Converted `Date` & `Time` → `DateTime`  
   - Extracted Year, Month, Day, Hour, DayOfWeek  

2. **Feature Engineering**
   - Created input-output features  
   - Applied `StandardScaler` for normalization  

3. **Model Building**
   - Used **Neural Network (Keras Sequential Model)**  
   - Layers: Dense(64, ReLU) → Dense(32, ReLU) → Dense(1)  

4. **Training**
   - Optimizer: `Adam`  
   - Loss: `MSE`  
   - Early Stopping to prevent overfitting  

5. **Evaluation**
   - Metrics: RMSE, MAE, R²  
   - Visualization of **Actual vs Predicted** values  

6. **Model Saving**
   - Trained model saved as `.h5`  
   - Can be reused for deployment  

---

## 📊 Results

- **RMSE:** ~0.19  
- **MAE:** ~0.12  
- **R² Score:** ~0.87  

✅ The model successfully predicts household power consumption with good accuracy.  

---

## 📈 Visualization

### Neural Network Predictions vs Actual
plt.savefig("images/nn_predictions.png")

---

## 🛠 Tech Stack
- **Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Scikit-learn, TensorFlow/Keras  
- **Tools:** Google Colab, GitHub  

---

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/sabnamjeny/powerpulse-energy-forecast.git
   cd powerpulse-energy-forecast
