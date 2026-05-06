#  Gold Price Prediction using Machine Learning

##  Overview
This project focuses on predicting **gold price variations** using machine learning and deep learning techniques. It evaluates multiple models to determine the most effective approach for financial time-series forecasting.

Using **10 years of historical gold price data**, the system applies preprocessing, feature engineering, and sequential modeling to generate accurate predictions.

---

##  Objectives
- Predict future gold prices using historical data  
- Compare multiple ML/DL models  
- Identify the best-performing algorithm  
- Improve accuracy using preprocessing & feature engineering  

---

##  Models Implemented
-  Random Forest Regressor  
-  Artificial Neural Network (ANN)  
-  Simple Recurrent Neural Network (RNN)  
-  Long Short-Term Memory (LSTM)  
-  Gated Recurrent Unit (GRU)  

---

##  Dataset
- **Source:** Yahoo Finance (`GC=F`)  
- **Time Period:** ~10 years (2016–2026)  
- **Features:**
  - Open, High, Low, Close prices  
  - Volume  

### Data Split
- Training: 80%  
- Testing: 20%  

---

##  Project Workflow

### 1. Data Acquisition
- Collected using `yfinance`
- Daily gold price records

### 2. Data Cleaning
- Removed unnecessary columns  
- Checked missing & duplicate values  
- Sorted data chronologically  

### 3. Feature Engineering
- Created technical indicators:
  - Moving Averages (SMA, EMA)
  - Daily Returns
  - MACD  

### 4. Data Preprocessing
- MinMax Scaling (0–1 normalization)
- Sliding window approach (30-day sequences)

### 5. Model Training
- All models trained on same dataset
- Ensures fair comparison

### 6. Evaluation Metrics
- MAE (Mean Absolute Error)
- MSE (Mean Squared Error)
- RMSE (Root Mean Squared Error)
- R² Score  

---

##  Results

| Model            | MAE (USD) | RMSE (USD) | R² Score |
|------------------|----------|-----------|----------|
|  GRU           | 118.20   | 161.16    | 0.88     |
|  LSTM          | 275.12   | 388.28    | 0.32     |
|  ANN           | 370.09   | 405.58    | 0.26     |
|  Random Forest | 542.15   | 707.29    | -1.26    |
|  Simple RNN    | 684.50   | 849.33    | -2.26    |

---

##  Key Insights
- GRU achieved the best performance across all metrics  
- LSTM performed well but slightly less efficient  
- ANN showed moderate accuracy  
- Random Forest & Simple RNN performed poorly  
- Time-aware models (GRU, LSTM) are best for financial forecasting  


##  Future Improvements
- Include macroeconomic indicators  
- Add sentiment analysis (news/social media)  
- Use hybrid deep learning models  
- Deploy real-time prediction system  
- Train on larger datasets  



##  Tech Stack
- Python  
- Pandas, NumPy  
- Scikit-learn  
- TensorFlow / Keras  
- Matplotlib / Seaborn





├── data/
├── notebooks/
├── models/
├── results/
├── README.md
└── requirements.txt




---

##  How to Run
1. Clone the repository  
```bash
git clone https://github.com/your-username/gold-price-prediction.git
cd gold-price-prediction



pip install -r requirements.txt


jupyter notebook

** Conclusion**

This project demonstrates that deep learning models, especially GRU, are highly effective
for predicting gold prices due to their ability to capture time-based patterns.
Model selection plays a critical role in financial forecasting accuracy.
---

## 📁 Project Structure
