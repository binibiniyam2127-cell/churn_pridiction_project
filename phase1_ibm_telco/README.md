# Phase 1: IBM Telco Churn Prediction

## Project Structure
phase1_ibm_telco/
├── config/ # Configuration files
├── data/ # Data directory
│ ├── raw/ # Raw data
│ └── processed/ # Processed data
├── models/ # Saved models
├── notebooks/ # Jupyter notebooks
├── reports/ # Generated reports
│ ├── figures/ # Visualizations
│ └── metrics/ # Performance metrics
├── scripts/ # ✅ Entry points
│ ├── run_pipeline.py # Main pipeline execution
│ ├── run_experiments.py # Hyperparameter tuning
│ ├── reports.py # Report generation
│ ├── data_preprocessing.py # Data preparation
│ └── model_serving.py # API serving
├── src/ # Source code
│ ├── data/ # Data loading
│ ├── features/ # Feature engineering
│ ├── models/ # Model training & calibration
│ ├── explainability/ # SHAP explanations
│ └── pipeline.py # Core pipeline logic
├── tests/ # Unit tests
├── logs/ # Log files
├── requirements.txt # Dependencies
└── README.md