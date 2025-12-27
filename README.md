# ✈️🤖 Flight Delay Prediction (Before Departure)

## 🚀 Summary
Built a machine learning model that predicts whether a flight will be **delayed by >15 minutes before takeoff** using U.S. domestic flight data from Kaggle (*Flight Status Prediction – Rob Mulla*).

The model uses **only pre-departure features** (no information leakage), making it suitable for **real operational use** by airlines.

---

## 🎥 Presentation (Google Slides)
Slides summarizing approach, results, and business value:

🔗 **Google Slides:**  
https://docs.google.com/presentation/d/1oKGXPa1kbt_gArrUnKjqEiHOtx-nQMgzA03brpFYgvk/edit?usp=sharing 

---

## 🎯 What this project shows
- Supervised classification on real aviation data  
- Feature engineering on high-cardinality categorical variables  
- Model comparison and metric-driven selection  
- Turning ML results into **business value**  

---

## 🧠 Problem
> Can we identify **high-risk flights before departure**?

This enables airlines to:
- reduce cascading network delays  
- plan crews and aircraft proactively  
- improve passenger communication  

---

## 📊 Results (Test Set)

| Model | ROC-AUC | Recall | Precision |
|------|--------|--------|-----------|
| Logistic Regression | ~0.66 | ~0.01 | ~0.63 |
| Random Forest | ~0.75 | ~0.16 | ~0.69 |
| **XGBoost** | **~0.76** | **~0.21** | ~0.67 |

👉 **XGBoost performed best overall**  
👉 Detects more delayed flights while keeping false alarms reasonable  

---

## 🗂 Dataset
- Kaggle — **Flight Status Prediction** (Rob Mulla)  
- ~563k flights, 120 columns  
- Multi-year U.S. domestic flights (~2018–2022)  
- Sampled **200k flights** for modeling efficiency  

### 🎯 Target variable
Delayed = 1 → arrival delay > 15 minutes
Delayed = 0 → otherwise
