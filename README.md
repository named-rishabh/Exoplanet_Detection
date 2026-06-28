# 🌌 Exoplanet Detection Challenge

<div align="center">

![Python](https://img.shields.io/badge/Python-3.14+-3776AB?style=for-the-badge\&logo=python\&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge\&logo=scikitlearn\&logoColor=white)
![CatBoost](https://img.shields.io/badge/CatBoost-FFD43B?style=for-the-badge)


### 🚀 Machine Learning Pipeline for Exoplanet Detection using Stellar Observations

*Predicting whether a star hosts an exoplanet using astronomical and transit features.*

---

</div>

## 📖 Overview

This repository contains my solution for the **Exoplanet Detection Challenge** organized by **Equinox – Astronomy Club, IIT Guwahati**.

The objective is to develop a robust machine learning pipeline capable of predicting whether a star hosts an exoplanet based on stellar characteristics and transit observations.

The project includes:

* 📊 Exploratory Data Analysis (EDA)
* 🧹 Data Cleaning & Missing Value Imputation
* ⚙️ Physics-based Feature Engineering
* 🤖 Training Multiple Gradient Boosting Models
* 📈 Model Evaluation
* 🏆 Submission File Generation

---

# 📂 Repository Structure

```text
.
├── Exoplanet_Detection.ipynb     # Complete notebook
├── submission.csv                # Final predictions
├── pyproject.toml
├── uv.lock
└── README.md
```

---

# 🛰 Dataset Features

The dataset contains both stellar and planetary properties, including:

| Category             | Examples                                |
| -------------------- | --------------------------------------- |
| ⭐ Stellar Properties | Radius, Temperature, Luminosity, Noise  |
| 🌍 Planet Properties | Radius, Orbital Period, Semi-major Axis |
| 🌞 Transit Features  | Transit Depth, Duration, SNR            |
| 🔭 Orbital Features  | Inclination, Eccentricity, Velocity     |
| 🌡 Derived Features  | Equilibrium Temperature, Flux Index     |

---

# ⚙️ Feature Engineering

Several physics-informed features were created and missing values were imputed using astrophysical relationships.

### Examples

### Radius Ratio

```python
rp_rs_ratio = sqrt(transit_depth_ppm / 1e6)
```

### Planet Radius

```python
planet_radius_re = rp_rs_ratio × stellar_radius_sr × 109.2
```

### Log Features

* log_period
* log_snr

### Physics-based Imputation

Missing values were estimated using known relationships between:

* Transit Depth
* Radius Ratio
* Stellar Radius
* Planet Radius
* Orbital Parameters

---

# 🤖 Models Used

The following models were trained and compared:

* ✅ CatBoostClassifier
* ✅ XGBoostClassifier
* ✅ LightGBMClassifier
* ✅ Random Forest
* ✅ Gradient Boosting
* ✅ Extra Trees

---

# 📈 Evaluation Metrics

Models were evaluated using:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

---

# 🛠 Tech Stack

| Library      | Purpose             |
| ------------ | ------------------- |
| Pandas       | Data Manipulation   |
| NumPy        | Numerical Computing |
| Scikit-Learn | ML Pipeline         |
| CatBoost     | Gradient Boosting   |
| XGBoost      | Gradient Boosting   |
| LightGBM     | Gradient Boosting   |
| Matplotlib   | Visualization       |
| Seaborn      | Statistical Plots   |

---

# 🚀 Getting Started

## Clone the repository

```bash
git clone https://github.com/named-rishabh/exoplanet-detection.git

cd exoplanet-detection
```

## Install dependencies

```bash
pip install -r requirements.txt
```

or

```bash
uv sync
```

---

# ▶️ Run the Notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open

```
Exoplanet_Detection.ipynb
```

Run all cells to reproduce the workflow and generate predictions.

---

# 📊 Machine Learning Workflow

```text
Dataset
   │
   ▼
Cleaning
   │
   ▼
Missing Value Imputation
   │
   ▼
Feature Engineering
   │
   ▼
Encoding
   │
   ▼
Train / Validation Split
   │
   ▼
Model Training
   │
   ▼
Evaluation
   │
   ▼
Hyperparameter Tuning
   │
   ▼
Prediction
   │
   ▼
submission.csv
```

---

# 💡 Highlights

* Physics-aware feature engineering
* Intelligent missing value imputation
* Multiple boosting algorithms
* Reproducible notebook
* Clean modular workflow
* Competition-ready submission

---

# 📌 Future Improvements

* Bayesian Hyperparameter Optimization
* Feature Selection
* Ensemble Learning
* SHAP Explainability
* Probability Calibration
* Cross Validation

---

# 📄 Results

The notebook generates a final prediction file:

```text
submission.csv
```

ready for submission to the competition leaderboard.

---

# 🤝 Contributing

Contributions are welcome!

Feel free to:

* Open an Issue
* Submit a Pull Request
* Suggest improvements

---

# ⭐ Support

If you found this project useful:

⭐ Star this repository

🍴 Fork it

🛰 Happy Exoplanet Hunting!

---

<div align="center">

### ✨ "Somewhere, something incredible is waiting to be known." — Carl Sagan

</div>
