# 🚗 Vehicle Fleet Reliability & Failure Analysis

A production-ready system for analysing vehicle fleet reliability, predicting component failures, and identifying safety risks — built with Python, SQLite, Plotly Dash, and scientific computing libraries.

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Plotly Dash](https://img.shields.io/badge/Dashboard-Plotly%20Dash-purple?logo=plotly)
![SQLite](https://img.shields.io/badge/Database-SQLite-green?logo=sqlite)

---

## 📦 Features

| Module | Description |
|--------|-------------|
| **Dataset Generator** | 100K+ synthetic vehicle repair records with realistic distributions |
| **ETL Pipeline** | Extract → Transform → Load with batch optimisation and ≥40% speed benchmark |
| **Weibull Analysis** | 2-parameter MLE fitting, reliability/hazard curves, B10/B50 life estimates |
| **ARIMA Forecasting** | Monthly failure volume & cost forecasts with anomaly detection |
| **Failure Analysis** | Pareto 80/20, repeat-failure rates, mileage×component heatmaps |
| **Safety Risk Scoring** | Weighted severity + repeat rate + growth trend → risk tiers |
| **K-Means Clustering** | Vehicle risk classification (Low / Medium / High / Critical) |
| **Interactive Dashboard** | 5-tab Plotly Dash app with filters, KPI cards, and drill-downs |
| **HTML Report** | Standalone reliability report with embedded interactive charts |

---

## 🗂 Project Structure

```
├── data/
│   ├── generate_dataset.py   # Synthetic data generator
│   └── fleet_repairs.db      # SQLite database (generated)
├── etl/
│   └── pipeline.py           # ETL pipeline with benchmarking
├── models/
│   ├── weibull_analysis.py    # Weibull reliability modelling
│   ├── forecasting.py        # ARIMA forecasting & anomaly detection
│   └── failure_analysis.py   # Pareto, heatmaps, risk scoring, clustering
├── dashboard/
│   └── app.py                # Multi-tab Plotly Dash dashboard
├── reports/
│   ├── generate_report.py    # HTML report generator
│   └── reliability_report.html  # Generated report
├── run_pipeline.py           # End-to-end orchestrator
├── requirements.txt
└── README.md
```

---

## 🚀 Quick Start

### 1. Install Dependencies

```bash
pip install -r requirements.txt
```

### 2. Run Full Pipeline + Dashboard

```bash
python run_pipeline.py
```

Then open **http://localhost:8050** in your browser.

### 3. Run Pipeline Only (No Dashboard)

```bash
python run_pipeline.py --no-dashboard
```

---

## 📊 Dashboard Tabs

| Tab | Content |
|-----|---------|
| **Fleet Overview** | KPI cards (total failures, avg cost, MTBF, reliability %), monthly trend, cost forecast |
| **Failure Trends** | Time-series chart filterable by make/model/year/region, Pareto analysis |
| **Component Risk Matrix** | Scatter plot (frequency vs severity) with Weibull B10 overlay, reliability & hazard curves |
| **Predictive Alerts** | ARIMA forecasts for top 10 components, threshold exceedance table, anomaly flags |
| **Safety Risk Register** | Color-coded risk tier table, K-Means vehicle clustering, drill-down to high-risk vehicles |

---

## ⚙ Tech Stack

- **Python** — pandas, NumPy, SciPy, statsmodels, scikit-learn
- **Database** — SQLite via SQLAlchemy
- **Visualisation** — Plotly, Dash, Dash Bootstrap Components
- **Reporting** — Jinja2 HTML templates with embedded Plotly charts
- **Reliability** — Weibull MLE (scipy.stats), ARIMA (statsmodels)

---

## 📄 License

MIT
