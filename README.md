# Strava 10K Race Prediction Project - Luigi Medrano

This project analyzes running data from Strava to predict 10K race performance. It includes **data cleaning, visualization, and machine learning models** to estimate your next 10K time and pace based on recent training.

## Project Structure

* `data/` – folder where you should place your Strava CSV export (note: this folder is included in `.gitignore` and not tracked in GitHub)
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
   https://github.com/lumedrano/Strava-Run-Prediction-Model.git
   cd Strava-Run-Prediction-Model
   ```
2. Create a `data/` directory in the project root (this folder is gitignored):

   ```bash
   mkdir data
   ```
3. Place your Strava CSV export in the `data/` folder and update file names if needed.

   * To get all of your Strava data in bulk for processing, follow this link: [Strava Bulk Export](https://support.strava.com/hc/en-us/articles/216918437-Exporting-your-Data-and-Bulk-Export#h_01GDP2C5E3278KM8MPK5X49ED3)
   * Scroll all the way down to the header **Bulk Export** and follow the directions to have your activity data emailed to you.
   * Unzip folder and export only the `activities.csv` file to the `data/` folder
4. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```
5. Open Jupyter notebooks in `notebooks/`:

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
* ML predictions are based on recent training trends (last 8 weeks).

## License

This project is open-source and free to use. Modify as needed for personal use or research.
