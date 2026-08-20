# 🎵 KKBox Churn Prediction Model

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![LightGBM](https://img.shields.io/badge/LightGBM-3.3+-green.svg)](https://lightgbm.readthedocs.io/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> Predict customer churn for KKBox music streaming platform with **97.4% accuracy** and **0.987 AUC**.

## 📊 Model Performance

| Metric | Value |
|--------|-------|
| **Accuracy** | 97.38% |
| **AUC-ROC** | 0.9866 |
| **Precision** | 84.42% |
| **Recall** | 86.96% |
| **F1-Score** | 85.67% |

## 🏗️ Project Structure

```
phase2_kkbox/
├── src/                    # Source code
│   ├── data/               # Data loading
│   ├── features/           # Feature engineering
│   ├── models/             # Model training
│   └── utils/              # Utilities
├── scripts/                # Pipeline scripts
├── config/                 # Configuration
├── notebooks/              # Jupyter notebooks
├── data/                   # Data directory
│   ├── raw/                # Raw data (not included)
│   └── processed/          # Processed data
├── models/                 # Trained models
├── reports/                # Reports and figures
└── requirements.txt        # Dependencies
```

## 🚀 Quick Start

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/kkbox-churn-prediction.git
cd kkbox-churn-prediction
```

### 2. Create virtual environment
```bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Download data
Place KKBox dataset files in `data/raw/`:
- `transactions_v2.csv`
- `user_logs_v2.csv`
- `members_v3.csv`
- `train_v2.csv`
- `sample_submission_v2.csv`

### 5. Run the pipeline
```bash
# Data cleaning
python scripts/02_preprocessing_cleaning.py

# Feature engineering
python scripts/03_feature_engineering.py

# Encoding
python scripts/05_encoding.py

# Model training
python scripts/06_train_model.py

# Evaluation
python scripts/08_evaluate_model.py

# SHAP analysis
python scripts/09_shap_analysis.py
```

## 📈 Pipeline Steps

| Step | Description | Output |
|------|-------------|--------|
| 1 | Data Loading | Load 28.5M rows |
| 2 | Data Cleaning | Handle missing values, outliers |
| 3 | Feature Engineering | 45+ features created |
| 4 | Data Split | 80/10/10 train/val/test |
| 5 | Encoding | 56 numeric features |
| 6 | Model Training | LightGBM (AUC: 0.987) |
| 7 | Calibration | Isotonic calibration |
| 8 | Evaluation | Test AUC: 0.9866 |
| 9 | SHAP Analysis | Feature importance |

## 🔧 Configuration

All parameters are centralized in `config/config.yaml`:
- Data paths and settings
- Model hyperparameters
- Feature engineering options
- Calibration settings

## 📊 Results

### Model Comparison
| Model | Validation AUC | Test AUC | Accuracy |
|-------|---------------|----------|----------|
| LightGBM | 0.9873 | 0.9868 | 97.41% |
| XGBoost | 0.9872 | 0.9867 | 96.26% |
| Random Forest | 0.9798 | 0.9788 | 96.48% |

### Key Churn Drivers (SHAP)
1. **avg_transaction_value** - Higher value → Higher churn
2. **tenure_days** - Longer tenure → Lower churn
3. **total_spent** - Higher spend → Higher churn
4. **engagement_score** - Lower engagement → Higher churn
5. **cancellation_count** - More cancellations → Higher churn

## 🛠️ Technologies Used

- **Language**: Python 3.8+
- **ML Frameworks**: LightGBM, XGBoost, Scikit-learn
- **Explainability**: SHAP
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Configuration**: YAML

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details.

## 👥 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📧 Contact

Your Name - your.email@example.com

Project Link: [https://github.com/yourusername/kkbox-churn-prediction](https://github.com/yourusername/kkbox-churn-prediction)
