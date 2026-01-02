# NYC-Taxi-Demand-Prediction
Predicting taxi demand in NYC using K-Means clustering for location segmentation and applying XGBoost for time-series forecasting to optimize fleet management.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](LINK_TO_YOUR_NOTEBOOK_HERE)

## Project Overview
This project applies Machine Learning to historical taxi trip data to predict the number of pickups in specific regions of NYC for the next 10-minute interval. Accurate forecasting helps in efficient fleet management, reducing wait times, and balancing supply with demand.

## Key Features
* **Clustering & Segmentation:** Used **Mini-Batch K-Means Clustering (K=30)** to group taxi pickup coordinates into 30 distinct geographical regions (clusters) for analysis.
* **Time-Series Analysis:**
    * Processed raw timestamps into **10-minute time bins**.
    * Analyzed weekly and daily seasonality patterns.
* **Feature Engineering:**
    * Created **Smoothing Features** using Simple Moving Averages and Weighted Moving Averages to reduce noise.
    * Engineered lag features to capture temporal dependencies.
* **Modeling:** Trained and evaluated multiple regression models, including **Linear Regression** and **XGBoost**, to minimize the Mean Absolute Error (MAE).

## Tech Stack
* **Language:** Python
* **Libraries:** Pandas, NumPy, Scikit-Learn, Dask (for large datasets), XGBoost, Folium (for map visualization).
* **Data Source:** NYC TLC Trip Record Data (Yellow Taxi).

## How to Run
The notebook is pre-rendered, so you can view all graphs, cluster maps, and predictions immediately without running the code.

If you wish to run the code yourself:
1.  Click the **"Open in Colab"** badge above.
2.  **Data Setup:** The notebook requires the NYC taxi dataset. You will need to upload your own `kaggle.json` (API Token) when prompted to download the data directly from Kaggle, or manually upload the CSV files.
3.  **High RAM Warning:** Clustering large datasets (millions of coordinates) is memory-intensive. If your Colab session crashes, try reducing the dataset size (sampling) or view the pre-calculated results.
4.  **Experiment:** Experiment with the code by opening in Colab(creates your own private copy).
