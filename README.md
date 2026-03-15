# Bank Stock Forecasting Project

This project explores how different modeling approaches perform in forecasting stock prices of major U.S. banks.  
The goal is to compare traditional econometric models, machine learning algorithms, and deep learning models when applied to financial time-series data.

The project was developed as part of a Business Data Analytics course.

---

## Dataset

The analysis focuses on three large U.S. banks:

- JPMorgan Chase (JPM)
- Bank of America (BAC)
- Wells Fargo (WFC)

The dataset spans roughly **2018–2025** and combines multiple sources of information:

Stock market data  
- Open  
- High  
- Low  
- Close  
- Volume  

Macroeconomic indicators  
- VIX (volatility index)  
- S&P 500 index  
- Federal Funds Rate  

Financial sentiment  
- sentiment scores derived from financial news  

These different signals were used together to study how external market conditions affect stock price movements.

---

## Data Processing

Before training the models, several preprocessing steps were applied:

- calculation of daily log returns  
- rolling volatility estimation  
- creation of lagged features  
- alignment of macroeconomic indicators with stock prices  
- handling of missing values  
- feature scaling when required  

Different preprocessing pipelines were used depending on the type of model.

---

## Models Implemented

The project compares three groups of models.

### Econometric Models

These models are commonly used in financial econometrics and provide interpretable structures.

- ARIMAX  
- SARIMAX  
- GARCH(1,1)  

They are mainly used to model price dynamics and volatility behavior.

---

### Machine Learning Models

Classical ML algorithms were applied for classification and volatility prediction tasks.

- Logistic Regression  
- Support Vector Machine (SVM)  
- Gradient Boosting Tree (LightGBM)  

These models help capture nonlinear relationships between features.

---

### Deep Learning Models

Recurrent neural networks were used for sequential prediction tasks.

- GRU  
- LSTM  
- LSTM with sentiment input  

These models are designed to learn temporal dependencies in financial time-series data.

---

## Evaluation Metrics

Regression models were evaluated using:

- RMSE  
- MAE  
- MAPE  

Classification models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1-score  

Time-series aware train/test splits were used to avoid data leakage.

---

## Key Observations

Some general observations from the experiments:

- No single model consistently performs best across all tasks.
- Econometric models remain useful for capturing macroeconomic effects.
- Machine learning models sometimes improve performance when nonlinear patterns exist.
- Deep learning models can perform well for short-term forecasting when enough temporal structure is present.

The impact of sentiment data was mixed and strongly depended on data quality and alignment.

---


## Installation

Clone the repository:
