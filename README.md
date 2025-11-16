# DS340W-Project-by-Haren-Anand
DS340W – Course Project
The Impact of Macroeconomic Variables on Quantitative Trading Performance Across Market Cycles

This GitHub repository is for academic purposes only. The materials uploaded here are part of a course project for DS340W – Applied Data Science, offered at The Pennsylvania State University (University Park, PA).

Repository Contents

This repository contains all relevant files used for our DS340W project.
All datasets and code have been referenced from their original sources, and appropriate credit is given below.

Datasets

macro_filled_final.xlsx – This dataset contains daily stock data combined with five key macroeconomic indicators (Federal Funds Rate, CPI YoY, Unemployment Rate, Yield Curve Slope 10Y–3M, and PMI Level).
The data was prepared and aligned with daily trading records for analysis in this project.

This project builds on the parent paper:
Wang, Yimeng & Yan, Keyue. (2023). “Machine learning-based quantitative trading strategies across different time intervals in the American market.” Quantitative Finance and Economics, 7(2): 276–295.  [10.3934/QFE.2023028](https://www.aimspress.com/article/doi/10.3934/QFE.2023028)


Code

DS340W_code.ipynb – This Jupyter Notebook performs the full analysis pipeline, including:

Importing and cleaning the macro-augmented dataset

Training multiple ML models (Decision Tree, SVM, Bagging, Random Forest, AdaBoost, CatBoost)

Predicting moving-average price changes

Converting regression outputs into trading signals

Evaluating performance using MAE, RMSE, and backtested returns

The code was adapted from the parent paper’s framework and the following Kaggle source:
Kaggle Notebook: Beat the Stock Market – The Lazy Strategy
 by Nicolas Carbone (cnic92)
 https://www.kaggle.com/code/cnic92/beat-the-stock-market-the-lazy-strategy/notebook

Modifications made:

Added macroeconomic indicators as new predictive features

Updated evaluation metrics to include performance comparison across different market cycles

Adjusted trading signal generation logic for macro-augmented predictions
