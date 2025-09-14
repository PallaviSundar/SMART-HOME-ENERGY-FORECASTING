# ⚡ Energy Consumption Forecasting in Smart Homes

## 📌 Project Overview
This project implements a **Smart Home Energy Consumption Forecasting System** using **Deep Learning (LSTM-inspired approach)**.  
The goal is to predict electricity usage (daily/hourly) based on historical consumption data, enabling homeowners to monitor and optimize their energy usage.

The interactive **web-based dashboard** allows users to:
- 📂 Upload energy consumption datasets (`.csv`, `.txt`, or `.zip` containing CSV/TXT).  
- 📊 Visualize historical energy usage trends.  
- 🔮 Forecast future consumption using LSTM-inspired logic.  
- 📉 Display key error metrics: **MAE, RMSE, MAPE**.  
- ⬇️ Download forecast results as CSV.  

---

## 🌍 Domain
- **Domain:** Deep Learning, Smart Home Energy Management  
- **Application:** Energy consumption forecasting & visualization  

---

## 🎯 Goal
- Develop an interactive **dashboard** for household energy forecasting.  
- Use **historical electricity usage** to predict future consumption patterns.  
- Help homeowners **analyze trends** and **plan energy-saving strategies**.  

---

## ✨ Features
1. **Data Upload & Parsing**
   - Accepts `.csv`, `.txt`, and `.zip` files.  
   - Automatically detects columns like `DateTime` and `Global_active_power`.  
   - Aggregates readings into **hourly values**.  

2. **Sample Data Generation**
   - Generates sample datasets with realistic daily & weekly consumption patterns.  

3. **Forecasting**
   - Predicts future energy usage with **LSTM-inspired simulation**.  
   - Supports custom forecast horizon (hours) and backtesting.  
   - Metrics calculated:  
     - **MAE** (Mean Absolute Error)  
     - **RMSE** (Root Mean Squared Error)  
     - **MAPE** (Mean Absolute Percentage Error)  

4. **Visualization**
   - Interactive **line charts** (historical vs forecasted consumption).  
   - KPIs explained with tooltips for better interpretation.  

5. **Download Forecast**
   - Export predictions as **CSV** for external analysis.  

---

## 🛠️ Technology Stack
- **Frontend:** HTML, CSS, JavaScript  
  - Chart.js → plotting  
  - PapaParse → CSV parsing  
  - Day.js → datetime handling  
  - JSZip → ZIP file extraction  

- **Backend:** Python, Flask  
  - Pandas → data processing  
  - Flask → file upload & API endpoints  

---

## 📂 File Structure

├── app.py # Flask backend
├── templates/
│ └── index.html # Dashboard frontend
├── static/ # Optional: CSS/JS files if separated
├── README.md # Project documentation


---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd <project-folder>

2. Install dependencies
pip install flask pandas

3. Run the Flask server
python app.py

4. Access the dashboard
http://127.0.0.1:5000/

5. Upload dataset or use sample data

Upload .csv, .txt, or .zip dataset.

Adjust parameters (horizon, backtest, days to load).

Click Run Forecast to generate predictions.

Download results as CSV if needed.


📊 Dataset

We use the Household Electric Power Consumption dataset:

Kaggle: [Download here](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)

UCI Repository: [Download here](https://archive.ics.uci.edu/ml/datasets/individual+household+electric+power+consumption)

🔹 Supported Dataset Formats

Original UCI Dataset

Columns: Date, Time, Global_active_power, Global_reactive_power,
Voltage, Global_intensity, Sub_metering_1, Sub_metering_2, Sub_metering_3

Preprocessed Dataset

Columns: DateTime, Global_active_power

(Optional: Voltage, Sub_metering, etc.)

🔸 Columns Used for Forecasting

DateTime (or Date + Time)

Global_active_power