# Medical Research Trend Forecasting using NLP (SBERT + BERTopic + Forecasting)

This project implements an end-to-end NLP-based framework to extract research topics from scientific literature and forecast how these topics evolve over time.

The pipeline converts large-scale research abstracts into monthly topic frequency time-series and predicts future topic prevalence using forecasting models.

---

## 📌 What This Project Does

This project solves the problem of:

> Automatically identifying research themes from scientific papers and predicting which topics are rising or declining over time.

It achieves this by combining:

- Transformer-based semantic embeddings (SBERT)
- Unsupervised topic modeling (BERTopic)
- Temporal aggregation (monthly topic frequency)
- Time-series forecasting (Prophet / ARIMA / LSTM)
- Forecast evaluation (MAE, RMSE, MAPE, Directional Accuracy)

---

## 🧠 Core Idea (Concept)

### Step 1 — Convert papers into semantic vectors
Instead of using only keywords, the system converts each paper’s **title + abstract** into a dense embedding using SBERT.

### Step 2 — Discover topics automatically
BERTopic clusters embeddings into topic groups and generates:

- topic keywords
- representative documents
- topic IDs

### Step 3 — Convert topics into time-series
Each topic is counted month-wise to generate a monthly frequency signal.

### Step 4 — Forecast future topic prevalence
Forecasting models predict the topic frequency into the future for horizons:

- 1 month
- 3 months
- 6 months
- 12 months

---

## 🏗️ Pipeline Overview

1. Dataset loading (peS2o / S2ORC)
2. Text preprocessing
3. SBERT embeddings generation
4. BERTopic topic extraction
5. Monthly topic aggregation
6. Forecasting using ARIMA / Prophet / LSTM
7. Evaluation and visualization

---


