# F1 2024 Season Analysis & Prediction

## Overview
This project is an in-depth exploratory data analysis (EDA) and predictive modeling initiative focused on the 2024 Formula 1 season. The goal is to analyze various performance metrics of drivers and teams and build a predictive model using XGBoost to estimate race results based on historical data.

## Features
### Exploratory Data Analysis (EDA)
The project covers multiple aspects of the 2024 season, including:
- **Drivers' Points Progression** throughout the season
- **Teams' Points Progression** throughout the season
- **Qualifying vs. Race Performance** analysis
- **Lap Time Trends** and **Average Relative Lap Time per Driver**
- **Driver Consistency** and **Position Changes** per race
- **Top Position Gainers** per race
- **Lap Performance of Top 3 Drivers** in each race
- **Tyre Stints Comparisons** for top drivers
- **Teammate Comparisons** (qualifying and race performance)
- **Average Finishing Positions** per driver and team
- **Track-based Comparisons** to highlight track-specific strengths
- **Pole Lap vs. 2nd Fastest Driver Lap** (speed, throttle, delta analysis)
- **Sector-wise Comparisons** for pole lap vs. 2nd fastest lap

### Data Processing & Feature Engineering
Data was collected from **FastF1**, the **official F1 website**, and other sources. Several additional features were derived, including:
- `AvgLapTime`, `FastestLapTime`, `RelativeLapTime`
- `TireStrategy`, `PitStopEfficiency`, `PitStopStdDev`
- `SafetyCarInfluence`, `QualifyingImpact`, `DeltaToPoleTime`
- Weather conditions (`AirTemp`, `TrackTemp`, `Rainfall`)
- Rolling averages for driver/team performance

### Machine Learning: XGBoost Model
The dataset was used to train an XGBoost model with hyperparameter tuning via `RandomizedSearchCV`. The pipeline includes:
- **Feature preprocessing:** Handling categorical & numerical variables
- **Hyperparameter tuning** for optimal model performance
- **Evaluation metrics:** Mean Squared Error (MSE), Mean Absolute Error (MAE), R-squared score (R²)

#### XGBoost Model Performance
- **Mean Squared Error:** 1.5213
- **Mean Absolute Error:** 0.6951
- **R-squared Score:** 0.9579

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/f1-2024-analysis.git
   cd f1-2024-analysis
   ```
2. Install required dependencies:
   ```sh
   pip install -r requirements.txt
   ```
3. Run the notebook:
   ```sh
   jupyter notebook F1_2024.ipynb
   ```

## Dependencies
Ensure you have Python 3.8+ installed along with the libraries listed in `requirements.txt`.

## Usage
- Run the notebook to explore the EDA visualizations.
- Modify `train_and_evaluate_xgboost_model()` to experiment with different features.
- Evaluate model performance using the test dataset.

## Future Improvements
- Implement **deep learning models** (LSTMs) for time-series performance prediction.
- Enhance **real-time race tracking** using live F1 APIs.
- Improve feature engineering for **better predictive accuracy**.

## License
This project is open-source under the MIT License.

---

