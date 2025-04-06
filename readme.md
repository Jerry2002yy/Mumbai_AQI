#  🌆 Mumbai AQI (Air Quality Index) Analysis 📊
This project analyze air pollution levels across 20 monitoring stations in Mumbai using data collected over time. The main goal is assess air quality, identify pollution trends, and apply machine learning to predict AQI levels based on key pollutant metrics.

---

## 📁  Project Structure 
Mumbai_aqi/ │ ├── Data/ # Folder with raw and merged data CSVs │ ├── <20 raw station CSVs> │ └── merged_air_quality.csv │ ├── Notebooks/ # Jupyter notebook(s) with complete workflow │ └── aqimumbai.ipynb │ ├── requirements.txt # Python dependencies ├── README.md # Project documentation


--- 

## 🔎 Project Overview 
- 🧾 **20 CSV files** were collected, each representing AQI data from a different Mumbai pollution monitoring station.
- 📊 Each file contains **7 key features**:
  - `Date`
  - `PM2.5`, `PM10`
  - `O₃`, `NO₂`, `SO₂`, `CO`

---

## 🔧 Analysis Steps

### 1. Data Import & Merging
- Loaded all 20 CSV files using 'pandas'.
- Added a 'Source_File' column to track station names.
- Merged all into a single DataFrame.

### 2. Feature Engineering 
- Applied **standard AQI formula** to calculate a unified AQI score.
-Added temporal feature (Month,Year)
- Removed outliers using IQR Method.

### 3. Exploratory Data Analysis (EDA)
- Visualized **average AQI over the years**
- Created a **correlation heatmap** to analyze realtionships between pollutants.
- Identified **top 10 most polluted stations**.
- Explored **monthly AQI variation** to detect seasonal trends.

### 4. Predictive Modeling
- Built regression models to predict AQI:
  - ✅ **XGBoost Regressor** – Delivered higher accuracy and lower error.
  - 🔁 **Linear Regression** – Used for comparison.

---

## 📊 Key Insights

- 📈 Certain stations consistently show higher pollution across all years.
- 🕒 AQI spikes during winter months.
- 💨 PM2.5 and NO₂ have the strongest correlation with AQI.
- 🤖 XGBoost proved more accurate for AQI prediction than linear models.

---

## 💻 Tech Stack

- **Language**: Python
- **Libraries**: Pandas, NumPy, Seaborn, Matplotlib, Scikit-learn, XGBoost
- **Tools**: Jupyter Notebook, Visual Studio Code

---

## 🙌 Contributing
Want to help improve this project?

1. Fork the repo

2. Create a new branch

3. Make your chages

4. submit a Pull Request