# 🔮 Customer Churn Prediction Project

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Random Forest](https://img.shields.io/badge/Random%20Forest-Tuned-brightgreen.svg)](https://scikit-learn.org/)
[![LightGBM](https://img.shields.io/badge/LightGBM-3.3+-green.svg)](https://lightgbm.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> End-to-end customer churn prediction with two real-world datasets.

## 📊 Overview

This repository contains two complete customer churn prediction projects:

| Phase | Dataset | Industry | Rows | Best Model | Accuracy | AUC |
|-------|---------|----------|------|------------|----------|-----|
| Phase 1 | IBM Telco | Telecommunications | 7,043 | Tuned Random Forest | ~83% | ~0.88 |
| Phase 2 | KKBox | Music Streaming | 970,960 | LightGBM + Isotonic | 97.38% | 0.9866 |

## 📁 Repository Structure

```
churn-prediction-project/
├── phase1_ibm_telco/          # Phase 1: IBM Telco
│   ├── src/                   # Source code modules
│   ├── scripts/               # Pipeline scripts
│   ├── notebooks/             # EDA and analysis
│   ├── config/                # Configuration
│   ├── data/                  # Data files
│   ├── models/                # Trained models
│   │   └── tuned_rf_model.joblib  # Best model
│   ├── reports/               # Reports and figures
│   ├── tests/                 # Unit tests
│   ├── README.md              # Project documentation
│   └── requirements.txt       # Dependencies
│
└── phase2_kkbox/              # Phase 2: KKBox
    ├── src/                   # Source code modules
    ├── scripts/               # Pipeline scripts
    ├── notebooks/             # EDA and analysis
    ├── config/                # Configuration
    ├── data/                  # Data files
    ├── models/                # Trained models
    ├── reports/               # Reports and figures
    ├── tests/                 # Unit tests
    ├── README.md              # Project documentation
    └── requirements.txt       # Dependencies
```

## 🚀 Quick Start

```bash
git clone https://github.com/yourusername/churn-prediction-project.git
cd churn-prediction-project
```

## 📊 Phase 1: IBM Telco

### Overview
Predict customer churn for IBM Telco dataset using Tuned Random Forest.

```bash
cd phase1_ibm_telco
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

### Results
| Model | Accuracy | Precision | Recall | F1-Score | AUC |
|-------|----------|-----------|--------|----------|-----|
| Tuned Random Forest | ~83% | ~83% | ~83% | ~83% | ~0.88 |
| LightGBM | ~81% | ~81% | ~81% | ~81% | ~0.85 |
| XGBoost | ~81% | ~81% | ~81% | ~81% | ~0.85 |
| Logistic Regression | ~79% | ~79% | ~79% | ~79% | ~0.82 |

## 🎵 Phase 2: KKBox

### Overview
Predict customer churn for KKBox music streaming platform with 970,960 customers.

```bash
cd phase2_kkbox
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python scripts/02_preprocessing_cleaning.py
python scripts/03_feature_engineering.py
python scripts/05_encoding.py
python scripts/06_train_model.py
python scripts/08_evaluate_model.py
python scripts/09_shap_analysis.py
```

### Results
| Metric | Value |
|--------|-------|
| Accuracy | 97.38% |
| AUC-ROC | 0.9866 |
| Precision | 84.42% |
| Recall | 86.96% |
| F1-Score | 85.67% |
| Brier Score | 0.0202 |

## 🛠️ Technologies Used

| Category | Technologies |
|----------|--------------|
| Languages | Python 3.8+ |
| ML Frameworks | Scikit-learn, LightGBM, XGBoost |
| Explainability | SHAP |
| Data Processing | Pandas, NumPy, Dask |
| Visualization | Matplotlib, Seaborn, Plotly |
| Configuration | YAML |
| Model Persistence | joblib, pickle |

## 📝 License

MIT License - see LICENSE file for details.

## 📧 Contact

Your Name - your.email@example.com

Project Link: https://github.com/yourusername/churn-prediction-project
