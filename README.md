#  MLOps Mini Pipeline (Crypto Signal Processing)

## Overview

This project implements a reproducible MLOps-style pipeline for processing cryptocurrency OHLCV data.
It computes rolling statistics, generates trading signals, and outputs structured metrics with logging and Docker-based deployment.

---

## Features

* Config-driven pipeline (YAML)
* Rolling mean computation
* Signal generation (binary trading signal)
* Structured JSON metrics output
* Logging with timestamps
* Error handling
* Docker containerization


## Project Structure
mlops-task/
├── run.py
├── config.yaml
├── data.csv
├── requirements.txt
├── Dockerfile
├── metrics.json
├── run.log
└── README.md

## ⚙️ Setup Instructions
pip install -r requirements.txt


## Run Locally
python run.py --input data.csv --config config.yaml --output metrics.json --log-file run.log

## Docker Usage
docker build -t mlops-task .
docker run --rm mlops-task

## Output Example (metrics.json)

json
{
  "version": "v1",
  "rows_processed": 10000,
  "metric": "signal_rate",
  "value": 0.49,
  "latency_ms": 120,
  "seed": 42,
  "status": "success"
}

## Dependencies

* pandas
* numpy
* pyyaml

## Key Concepts Demonstrated

* Reproducibility using seed
* Data validation
* Feature engineering (rolling mean)
* Observability (logging)
* Containerized deployment (Docker)

---

## Use Case
This project simulates a real-world MLOps pipeline used in algorithmic trading systems for signal generation and monitoring.

## Author

Aditya Raj Singh
B.Tech Electronics System Engineering
