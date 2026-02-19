# 🏎️ F1 Qualifying Performance Predictor

**Status:** 🚧 In Progress | **Level:** Beginner → Intermediate

> Predict Formula 1 qualifying positions using machine learning regression models based on practice session performance data.

---

## 🎯 Project Overview

This project uses linear regression to predict where drivers will qualify based on their practice session performance. It introduces fundamental machine learning concepts including:
- Train/test splitting
- Feature engineering
- Model evaluation metrics
- Cross-validation

### Key Questions:
- Can practice session times predict qualifying performance?
- Which practice session is most predictive? (FP1, FP2, FP3)
- How do track conditions affect predictions?
- What features matter most for qualifying success?

---

## 💡 Motivation

After analyzing lap times in my [F1 Lap Time Analyzer](https://github.com/webdevluis0510/f1-lap-analyzer), I wanted to take the next step: **using data to make predictions**. This project introduces machine learning fundamentals while staying in the F1 domain I'm specializing in.

**Why Qualifying Prediction?**
- Clear target variable (qualifying position)
- Rich feature set (FP times, sectors, weather)
- Real-world application (teams do this!)
- Foundation for more complex models

---

## 📊 Technical Approach

### Data Collection
- **Source:** FastF1 API
- **Sessions:** FP1, FP2, FP3, Qualifying
- **Features:** Best lap times, sector times, tire compounds, track temperature

### Feature Engineering
Key features to extract:
- Best lap time in each practice session
- Sector time averages
- Tire compound used for fast laps
- Track evolution (session improvement)
- Weather conditions
- Team performance (relative to teammate)

### Model
- **Algorithm:** Linear Regression (scikit-learn)
- **Target:** Qualifying position (1-20)
- **Evaluation:** MAE, RMSE, R²

### Workflow
1. Collect data from multiple races (2024-2025 season)
2. Feature engineering (practice → qualifying features)
3. Train/test split (80/20)
4. Train linear regression model
5. Evaluate on test set
6. Feature importance analysis

---

## 🛠️ Tech Stack

- **Python 3.x** - Programming language
- **FastF1** - F1 data API
- **Pandas & NumPy** - Data manipulation
- **Scikit-learn** - Machine learning
- **Matplotlib/Seaborn** - Visualization
- **Jupyter Notebook** - Development environment

---

## 📁 Project Structure
```
f1-qualifying-predictor/
├── data/
│   ├── raw/              # Raw FastF1 data
│   └── processed/        # Cleaned, feature-engineered data
├── notebooks/            # Jupyter notebooks for analysis
├── models/               # Saved trained models
├── outputs/
│   ├── charts/          # Visualizations
│   └── reports/         # Analysis reports
├── cache/               # FastF1 cache
└── README.md
```

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8+
- pip package manager

### Installation
```bash
# Clone repository
git clone https://github.com/webdevluis0510/f1-qualifying-predictor.git
cd f1-qualifying-predictor

# Create virtual environment
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Mac/Linux

# Install dependencies
pip install -r requirements.txt
```

### Usage
```bash
# Start Jupyter Notebook
jupyter notebook

# Open notebooks in order:
# 01_data_collection.ipynb
# 02_exploratory_analysis.ipynb
# 03_feature_engineering.ipynb
# 04_model_training.ipynb
# 05_evaluation.ipynb
```

---

## 📈 Expected Results

*Will be updated as analysis progresses*

### Model Performance Goals:
- **MAE:** < 3 positions (predicting within 3 spots)
- **RMSE:** < 4 positions
- **R²:** > 0.6 (explaining 60%+ of variance)

### Key Insights:
- Which practice session is most predictive?
- How much does FP1 vs FP3 matter?
- Impact of track conditions
- Feature importance rankings

---

## 🎓 What I'm Learning

### Machine Learning Fundamentals:
- Train/test splitting
- Linear regression implementation
- Model evaluation metrics (MAE, RMSE, R²)
- Feature scaling and normalization
- Cross-validation basics

### Data Science Skills:
- Feature engineering from raw data
- Handling temporal data (session → session)
- Dealing with missing values
- Outlier detection and handling

### Domain Application:
- F1 qualifying format and rules
- Practice session dynamics
- Track evolution effects
- Team performance patterns

---

## 🔮 Future Enhancements

- [ ] Add classification (will driver reach Q2/Q3?)
- [ ] Include weather forecast data
- [ ] Compare multiple ML algorithms
- [ ] Feature importance visualization
- [ ] Prediction confidence intervals
- [ ] Real-time predictions during race weekend

---

## 🔗 Related Projects

- **[F1 Lap Time Analyzer](https://github.com/webdevluis0510/f1-lap-analyzer)** - Foundation project (data analysis)
- **[F1 Tire Degradation Predictor](https://github.com/webdevluis0510/f1-tire-degradation-predictor)** - Next step (advanced ML)

---

## 📚 Learning Resources

- **Scikit-learn Documentation:** https://scikit-learn.org/
- **FastF1 API Docs:** https://docs.fastf1.dev/
- **Introduction to Statistical Learning** (ISLR book)
- **Kaggle Learn:** ML courses

---

## 📧 Contact

Luis - [GitHub](https://github.com/webdevluis0510)

**Portfolio:** Building toward Applied ML Systems Engineer specializing in F1 performance optimization.

---

*This project is part of my structured path: Data Analysis → ML Engineering → ML Systems Engineering, with deep specialization in Formula 1 motorsports.*