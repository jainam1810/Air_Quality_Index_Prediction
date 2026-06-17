
# Mumbai AQI Dashboard

A real-time, interactive Air Quality Index (AQI) dashboard for **Mumbai**, built using **Streamlit**, **scikit-learn**, and **Folium**. It fetches live air quality data from the **Central Pollution Control Board (CPCB)** and uses a trained **Random Forest** model to predict AQI values when missing.

---

## Features

Fetches real-time AQI data from CPCB’s RSS XML feed  
✅ Predicts missing AQI values using a trained machine learning model  
✅ Visualizes station-wise AQI data on an interactive map using Folium  
✅ Displays pollutant-specific statistics in a clean tabular format  
✅ Highlights AQI severity with color-coded markers (Green to Maroon)

---

## 🧠 ML Model Overview

The application uses a `RandomForestRegressor` trained on historical AQI data with the following setup:

- **Input Features**:  
  - PM2.5  
  - PM10  
  - NO₂  
  - SO₂  
  - CO  
  - O₃

- **Preprocessing Pipeline**:
  - Missing values handled using `SimpleImputer`
  - Features normalized using `StandardScaler`

- **Saved Artifacts**:
  - `imputer.pkl`
  - `scaler.pkl`
  - `rf_model.pkl`

---

## 📁 Project Structure

```

mumbai-aqi-dashboard/
├── app.py                # Main Streamlit app file
├── imputer.pkl           # Trained SimpleImputer object
├── scaler.pkl            # Trained StandardScaler object
├── rf\_model.pkl          # Trained Random Forest model
├── requirements.txt      # List of required Python packages
├── README.md             # Project documentation
└── .gitignore            # Git ignore file

````

---

## 📦 Installation

### 🔧 Prerequisites

- Python 3.7 or later
- pip

### 🛠 Setup Instructions

```bash
# 1. Clone the repository
git clone https://github.com/kartikeyadangat/AQI-Prediction.git
cd mumbai-aqi-dashboard

# 2. Install the required packages
pip install -r requirements.txt

# 3. Run the Streamlit app
streamlit run app.py
````

---

## 🗺️ Live Preview

The application interface includes:

* 📊 A clean table of pollutant values per station
* 🗺️ A folium map with color-coded AQI markers
* 🔄 Auto-calculated predictions when AQI data is missing

---

## 🎨 AQI Color Scale

| AQI Range | Color       | Meaning      |
| --------- | ----------- | ------------ |
| 0–50      | Green       | Good         |
| 51–100    | Light Green | Satisfactory |
| 101–200   | Orange      | Moderate     |
| 201–300   | Red         | Poor         |
| 301–400   | Purple      | Very Poor    |
| 401+      | Maroon      | Severe       |

---

## 📦 Dependencies

Listed in `requirements.txt`:

```txt
streamlit
pandas
numpy
joblib
scikit-learn
folium
requests
streamlit-folium
```

Install them all with:

```bash
pip install -r requirements.txt
```

---

## 🖼️ Screenshots (Optional)

You can add screenshots in a folder called `images/` and reference them like:

```markdown
![Dashboard Preview](images/dashboard.png)
![Map View](images/map.png)
```


