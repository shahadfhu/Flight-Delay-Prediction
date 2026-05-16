# Flight Delay Prediction

> A machine learning project that predicts whether a flight will be delayed (15+ minutes) before departure.

---

## About This Project

Flight delays are a headache for everyone — passengers miss connections, airlines lose money, and airports struggle to manage the chaos. This project explores whether we can **predict delays before they happen** using historical flight data.

We analyzed around **485,000 flight records** and tested multiple ML models to find the best approach.

---

## Dataset

Used the [Flight Delay and Causes](https://www.kaggle.com/datasets/undersc0re/flight-delay-and-causes) dataset from Kaggle.

| Stat | Value |
|------|-------|
| Total flights | ~485,000 |
| On-time | ~52% |
| Delayed (15+ min) | ~48% |

**Features used:**
- When: flight date, departure time, day of week
- Where: origin airport, destination, distance
- Who: airline carrier
- Historical delay causes: weather, carrier issues, security, etc.

---

## Models Compared

| Model | F1-Score | ROC-AUC |
|-------|----------|---------|
| Logistic Regression | 0.572 | 0.631 |
| Random Forest | 0.626 | 0.690 |
| **XGBoost** | **0.643** | **0.708** |
| Neural Network | 0.637 | 0.687 |

**XGBoost** came out on top — about **12% better than the baseline**, correctly catching ~65% of delays before they happen.

---

## Results (XGBoost)

| Metric | Value |
|--------|-------|
| Correctly predicted delays | 45,852 |
| Correctly predicted on-time | 48,612 |
| False alarms | 26,657 |
| Missed delays | 24,245 |

Catching two-thirds of delays in advance is practically valuable for travel planning and airline operations.

---

## How to Run

**Option 1 — Google Colab (recommended):**

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lKX6XmT3vFhQI9dvFC14eVdA_WjoEtvL?usp=sharing)

**Option 2 — Run locally:**

```bash
git clone https://github.com/YOUR_USERNAME/flight-delay-prediction.git
cd flight-delay-prediction
pip install pandas numpy scikit-learn xgboost matplotlib seaborn
jupyter notebook flight_delay_prediction.ipynb
```

---

## Team

This was a group project for **ML 4552** at Prince Sattam bin Abdulaziz University.

| Name |
|------|
| Noura Aldossari  |
| Haneen Aldossari |
| Shahad Aldawish  |
| Ebtihal Alharthi |

**Supervised by:** Dr. Haya Alaskar

---

## Links

- [Colab Notebook](https://colab.research.google.com/drive/1lKX6XmT3vFhQI9dvFC14eVdA_WjoEtvL?usp=sharing)
- [Dataset on Kaggle](https://www.kaggle.com/datasets/undersc0re/flight-delay-and-causes)
