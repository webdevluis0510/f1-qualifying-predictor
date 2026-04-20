# F1 Qualifying Performance Predictor

**Status:** Complete | **Level:** Beginner → Intermediate

A machine learning project that predicts Formula 1 qualifying positions using practice session performance data.

---

## Project Overview

This project uses linear regression to predict where drivers will qualify based on their lap times from Free Practice sessions (FP1, FP2, FP3). The model analyzes historical F1 telemetry data to identify patterns between practice performance and qualifying results.

### Key Questions Addressed:
- Can practice session times predict qualifying performance?
- Which practice session is most predictive?
- How accurately can we forecast qualifying positions?

---

## Technical Approach

### Data Collection
- **Source:** FastF1 API
- **Race Weekend:** Monaco 2025
- **Sessions:** FP1, FP2, FP3, Qualifying
- **Features:** Best lap time from each practice session per driver

### Feature Engineering
- Extracted fastest lap time for each driver from each practice session
- Filtered out invalid laps (pit stops, incomplete laps)
- Converted lap times to seconds for numerical processing
- Merged practice data with qualifying positions

### Model
- **Algorithm:** Linear Regression (scikit-learn)
- **Target Variable:** Qualifying position (1-20)
- **Input Features:** FP1 best time, FP2 best time, FP3 best time
- **Train/Test Split:** 80% training, 20% testing

### Evaluation
Predictions evaluated using:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R-squared Score

---

## Results

### Model Performance:
- **MAE:** 3.16 positions
- **RMSE:** 14.59 positions
- **R² Score:** 0.76 (explains 76% of variance)

### Key Findings:
- Model achieved strong predictions for front-runners (P1-P5) due to consistent performance
- Mid-field positions (P12-P19) were harder to predict due to higher variability
- Average prediction error of approximately 3 positions is reasonable given limited feature set
- Single large error (P18 predicted as P12) significantly impacted MAE

---

## Tech Stack

- **Python 3.x** - Programming language
- **FastF1** - F1 data API
- **Pandas & NumPy** - Data manipulation
- **Scikit-learn** - Machine learning
- **Matplotlib** - Visualization
- **Jupyter Notebook** - Development environment

---

## Project Structure