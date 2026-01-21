# LSTM-Stock-Prediction-Model
## Overview
This project develops a Multi-Scale LSTM–based framework for stock price prediction, motivated by the limitations of single-scale time-series models in capturing both short-term fluctuations and long-term market trends. The work was originally completed as part of the International Mathematical Modeling Challenge (IM2C).

Traditional LSTM models rely on a fixed lookback window, which can lead to biased learning: short windows emphasize local noise, while long windows may smooth out important short-term dynamics. To address this issue, we construct multiple LSTM models operating at different temporal scales (30, 45, and 60 days) and integrate their predictions into a unified forecasting framework.

We first evaluate single-scale LSTM models and a naïve multi-scale ensemble that averages their predictions. While the averaged multi-scale model improves stability, it does not consistently outperform the best single-scale model. To further enhance predictive accuracy, we introduce a linear regression layer that learns optimal weights for combining outputs from different LSTM scales. This results in a final Multi-Scale LSTM with Linear Regression (LSTM-LR) model.

Experiments are conducted using historical stock data from Ford Motor Company (F), including open, close, high, low prices, and trading volume. Model performance is evaluated using Mean Absolute Error (MAE) and Mean Squared Error (MSE). Results show that the proposed LSTM-LR model significantly reduces prediction error compared to both single-scale LSTM models and simple multi-scale averaging, demonstrating the effectiveness of learning scale-dependent contributions explicitly.

Overall, this project highlights how multi-scale temporal modeling combined with a lightweight statistical fusion layer can improve robustness and accuracy in financial time-series prediction, while remaining flexible and extensible to other assets and forecasting horizons.

## 📄 Project Report

👉 [Click here to view the project report](https://JamesGuo111.github.io/Multi-Scale-LSTM-Model-for-Stock-Prediction/report.pdf)

