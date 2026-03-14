# Strava 10K Race Prediction Project - Luigi Medrano

This project analyzes running data from Strava to predict 10K race performance. It includes **data cleaning, visualization, and machine learning models** to estimate your next 10K time and pace based on recent training.

## Project Structure

* `data/` – cleaned CSV data exported from Strava
* `notebooks/` – Jupyter notebooks for data loading, visualization, and 10K prediction

  * `data_visualization.ipynb` – explores running data: pace over time, distance distribution, weekly mileage, and performance curves
  * `prediction_model.ipynb` – ML-based and Riegel formula predictions for 10K
* `README.md` – project overview and instructions

## Features

1. **Data Cleaning & Preprocessing**

   * Converts distance to miles and calculates pace (min/mile)
   * Filters relevant columns from Strava exports
   * Handles recent training periods (last 8 weeks) for personalized predictions

2. **Data Visualization**

   * Pace over time
   * Distance distribution
   * Weekly mileage trends
   * Performance curve (fastest pace vs distance)
   * Comparison of predicted vs recent pace

3. **10K Prediction**

   * Baseline prediction using **Riegel formula**
   * ML model using recent training features:

     * Fastest pace in 3–7 mile runs
     * Average recent pace
     * Maximum distance
     * Total mileage in the last 8 weeks
   * Outputs predicted 10K time and pace
   * Visualizes predictions vs recent training

## How to Use

1. Clone the repository:

   ```bash
   git clone https://github.com/<username>/10k-prediction.git
   cd 10k-prediction
   ```
2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
3. Place your Strava CSV export in the `data/` folder and update file names if needed.
4. Open Jupyter notebooks in `notebooks/`:

   * Run `data_visualization.ipynb` to explore your data.
   * Run `prediction_model.ipynb` to see predictions for your next 10K.

## Dependencies

* pandas
* numpy
* matplotlib
* seaborn
* plotly
* scikit-learn

## Notes

* All distances are converted to **miles**, pace is in **minutes per mile**.
* Predictions assume consistent training; additional long runs or tempo sessions may improve estimates.
* ML predictions are based o
