# 📈 Predictive Early Warning System for Customer Churn (Telco)

This repository contains the code and Machine Learning analysis for building a **Predictive Early Warning System** to detect customer churn risk in the telecommunications industry. 

The project utilizes the **CatBoost** algorithm and the *Kaggle Telecom Churn Case Study* dataset, focusing on detecting danger signals a full month before a customer actually switches to a competitor.

## Project Objective
In the hyper-competitive telecommunications industry, retaining an existing customer is significantly cheaper (up to 5x) than acquiring a new one. 
This project aims to shift the churn management approach from **reactive** (acting after the customer leaves) to **proactive** (anticipating and acting early based on usage drop signals).

## Tech Stack & Tools
* **Dataset**: Kaggle Telecom Churn Hackathon
* **Predictive Model**: CatBoost Classifier
* **AI Interpretation**: SHAP (SHapley Additive exPlanations)
* **Languages & Libraries**: Python, Pandas, Scikit-Learn, Matplotlib

## Business Insights
Rather than solely chasing overall *Accuracy*, this model is built with a deep understanding of the business domain:
1. **Focus on Recall (70.3%)**: The model is optimized to catch as many high-risk customers as possible. We intentionally sacrificed a bit of *Precision* because the cost of sending retention promos to the wrong targets (False Positives) is far cheaper than letting actual customers leave unnoticed (False Negatives).
2. **Strongest Warning Signals**: Based on our SHAP analysis, a short loyalty tenure (*Age on Network*) and sudden *usage drops* in the 7th month are the absolute strongest indicators that a customer will churn in the 8th month.

## Read More
For a comprehensive breakdown covering Exploratory Data Analysis (EDA), imbalanced data strategies, and translating AI metrics into business reality, please read my full article on Medium:
[From Usage Drops to Retention: Building an Early Warning Churn System with CatBoost](https://medium.com/@andrew.parulian1/from-usage-drops-to-retention-building-an-early-warning-churn-system-with-catboost-f2e7b239fafe?postPublishedType=repub)
