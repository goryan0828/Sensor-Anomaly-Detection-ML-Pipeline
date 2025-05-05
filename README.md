# Sensor Anomaly Detection ML Pipeline

## Overview

Designed and implemented a production-grade machine learning pipeline to detect
anomalies in sensor telemetry data, simulating real-world scenarios in
manufacturing and system health monitoring. The project demonstrates strong
engineering practices across data preprocessing, model development, MLOps
automation, and API deployment.

## Key Contributions

- Built a modular Python-based pipeline for anomaly detection using
  time-series sensor data.

- Engineered robust preprocessing workflows and feature extraction logic
  for synthetic and open telemetry datasets.

- Trained and evaluated baseline ML models (e.g., Isolation Forest, XGBoost)
  and logged experiments using MLflow.

- Developed a FastAPI service to serve real-time inferences via Dockerized
  REST endpoints.

- Designed an automated retraining pipeline using Airflow, simulating
  data drift and scheduled updates.

- Integrated model versioning, performance tracking, and optional drift
  detection via EvidentlyAI.

## Tech Stack

Python, Pandas, Scikit-learn, XGBoost, MLflow, FastAPI, Docker, Airflow (or
Prefect), EvidentlyAI

## Highlights

- Simulates a full ML lifecycle: ingestion → training → monitoring → serving

- Reproducible and infrastructure-aligned: emphasizes DevOps and automation
  for ML

- Demonstrates strengths in scalable pipeline design, versioning,
  and real-time systems integration

This project implements a full ML pipeline to detect anomalies in simulated
sensor (telemetry) data. It demonstrates best practices for machine learning
infrastructure including:

- Data ingestion and preprocessing

- Model training and versioning with MLflow

- Automated retraining workflow

- Model serving with FastAPI and Docker

## Project Structure

```python
data/                   # Raw and processed data files
notebooks/              # Exploratory Data Analysis (EDA) and 
                        # development notebooks
src/
  preprocessing/        # Scripts for cleaning and feature extraction
  training/             # Training and evaluation scripts
  inference/            # Inference logic for deployment
api/                    # FastAPI app to serve predictions
configs/                # Config files for parameters, paths
```python

## Stack

- Python, pandas, scikit-learn, xgboost

- MLflow for experiment tracking

- FastAPI for model serving

- Airflow/Prefect for orchestration

- Docker for packaging

## Getting Started

1. Install dependencies (TBD)
2. Run preprocessing: `python src/preprocessing/preprocess.py`
3. Train the model: `python src/training/train.py`
4. Start the API server: `uvicorn api.app:app --reload`
5. Track experiments in MLflow UI: `mlflow ui`

## 📍 Project Roadmap

- [x] Phase 1: Project Setup & Data Simulation

  - Set up folder structure and README

  - Create/generate synthetic sensor dataset

  - Implement basic preprocessing and EDA

- [ ] Phase 2: Baseline Model Training

  - Train initial model (e.g., Isolation Forest/XGBoost)

  - Log metrics and models using MLflow

  - Evaluate baseline performance

- [ ] Phase 3: Model Serving

  - Create FastAPI app to serve predictions

  - Dockerize the API and test endpoints

  - Add simple usage docs in the README

- [ ] Phase 4: Automation & Retraining

  - Use Airflow/Prefect to schedule periodic retraining

  - Automate pipeline: preprocess → train → register model

  - Log retrain jobs and monitor changes

- [ ] Phase 5: Drift Detection & Monitoring

  - Integrate EvidentlyAI or similar for drift detection

  - Alert/log when drift exceeds threshold

  - Add observability hooks (logging, dashboards)

- [ ] Phase 6: Final Polish

  - Clean up repo structure

  - Finalize documentation and screenshots

  - Tag release and share publicly

## License

MIT License
