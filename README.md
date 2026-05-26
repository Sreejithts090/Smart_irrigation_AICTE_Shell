# Smart Farm Irrigation System 🌾🤖

[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org)
[![Framework](https://img.shields.io/badge/Framework-Streamlit-FF4B4B.svg)](https://streamlit.io)
[![Machine Learning](https://img.shields.io/badge/ML-Scikit--Learn-F7931E.svg)](https://scikit-learn.org)
[![Internship](https://img.shields.io/badge/Program-Shell--Edunet%20Skills4Future-green.svg)](https://edunetfoundation.org)

An end-to-end smart agriculture solution built during the **Shell-Edunet Skills4Future Virtual Internship** (organized by AICTE, Shell India, and Edunet Foundation) under the specialization of *Artificial Intelligence and Data Analytics focused on Green Skills*.

This project leverages Machine Learning to optimize water conservation and distribution by analyzing real-time sensor matrices across multiple farm sectors to automate irrigation pump actions.

---

## 📌 Project Overview

Traditional irrigation methods often lead to either over-watering or under-watering, causing structural crop damage and massive water waste. This project addresses these environmental and agricultural issues by implementing a predictive backend that evaluates **20 distinct environmental and soil sensor data streams**. 

The system utilizes a multi-label classification model to control **three independent irrigation zone pumps (`parcel_0`, `parcel_1`, `parcel_2`) simultaneously**, shifting resource management from manual schedules to automated, data-driven precision.

---

## 🛠️ Tech Stack & Key Libraries

* **Core Programming:** Python
* **Machine Learning Backend:** Scikit-Learn (MultiOutputClassifier, RandomForestClassifier)
* **Data Pipelines & Analytics:** Pandas, NumPy
* **Data Preprocessing:** MinMaxScaler
* **Model Serialization:** Joblib
* **Interactive Frontend:** Streamlit Dashboard
* **Visualizations:** Matplotlib, Seaborn

---

## 🧠 Machine Learning Pipeline

1. **Exploratory Data Analysis (EDA):** Analyzed correlations across a 20-sensor array capturing environmental and moisture data matrices.
2. **Data Preprocessing:** Extracted target vectors and normalized feature distributions using `MinMaxScaler` to guarantee stable gradient boundaries.
3. **Model Engineering:** Wrapped a tuned `RandomForestClassifier` inside a `MultiOutputClassifier` to enable simultaneous, distinct binary logic arrays across three independent targeted pump zones.
4. **Performance Evaluation:** Validated using precision, recall, and F1-score evaluation metrics, achieving a multi-label macro precision score of **90%**.
5. **Serialization:** Saved the final pipeline as a serialized payload (`Farm_Irrigation_System.pkl`) for minimal inference latency during production routing.

---

## 🖥️ App Dashboard Features

The deployment application built with **Streamlit** introduces an accessible control bridge for modern farming:
* **Real-time Diagnostics:** Input field matrices simulating 20 hardware sensors tracking zone metrics.
* **Predictive Automation:** Instantaneous processing triggers determining exact `ON / OFF` states for individual parcel pumps.
* **Analytical Insights:** Clear visual status reporting mapped out to prevent unnecessary water usage.

---

## 📁 Repository Structure

```text
├── irrigation_System1.ipynb   # Jupyter Notebook containing data preprocessing, EDA, and ML model training
├── Farm_Irrigation_System.pkl # Serialized production-ready model pipeline (Joblib payload)
├── app.py                     # Streamlit application file for the interactive user dashboard
├── requirements.txt           # Required environments dependencies
└── README.md                  # Project documentation
