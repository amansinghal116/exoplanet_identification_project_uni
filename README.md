# 🪐 ExoML: Exoplanet Identification Using Machine Learning

## 🌌 Project Overview

This project explores how **machine learning techniques** can be applied to data from NASA’s **Kepler Space Observatory** to distinguish between **confirmed exoplanets** and **candidate signals**.  

Our objectives were to answer three key questions:
1. How accurately can we classify exoplanets using machine learning?
2. Which features are most influential in exoplanet detection?
3. Can our models provide deeper insights to improve future surveys?

We evaluated several approaches — **classical models**, **tree-based methods**, **ensemble algorithms**, and **neural networks**. Among these, **Gradient Boosting** performed best, achieving an accuracy of **83.6%**. Key predictors included **signal-to-noise ratio** and **transit duration**, both critical in identifying genuine exoplanets.

These findings have the potential to guide researchers in **improving survey strategies** and **identifying habitable worlds** more efficiently.

---

## 📊 Dataset Information

- **Source:** [Kaggle - Kepler Exoplanet Search Results](https://www.kaggle.com/datasets/nasa/kepler-exoplanet-search-results)  
- **Provider:** NASA / Kepler Space Telescope  
- **Task:** Classification of exoplanet status (CONFIRMED vs CANDIDATE)

---

## 🌠 Introduction

**Exoplanets** are planets that orbit stars beyond our solar system. Detecting these distant worlds relies on a variety of methods, primarily:

- **Transit Method** 🌓 — Observing the **slight dimming of a star’s light** when an exoplanet passes in front of it.  
- **Radial Velocity** 🌍 — Detecting the **star’s wobble** due to gravitational pull from orbiting planets.

In 2009, **NASA launched the Kepler Space Telescope** to accelerate the discovery of exoplanets. Kepler monitored stars for tiny dips in brightness, signaling potential planets. With the growing amount of observational data, manual analysis became increasingly challenging.

**Machine learning offers a scalable, accurate solution** for classifying exoplanets using patterns in the data. By leveraging Kepler’s dataset and applying algorithms such as Logistic Regression, KNN, SVM, Decision Trees, Neural Networks, Random Forest, and Gradient Boosting, we can:

- Distinguish between real and false signals,  
- Prioritize promising candidates,  
- Support the search for habitable planets beyond our solar system.

---

## 🧾 Database Details

### 🆔 KOI Identification  
- **Fields:** `kepid`, `kepoi_name`, `kepler_name`  
- **Description:** KOI (Kepler Object of Interest) indicates a target showing transit-like patterns, suggesting potential planets.

---

### 📌 Status  
- **Field:** `koi_disposition`  
- **Values:** `CANDIDATE`, `CONFIRMED`  
- **Use:** This column serves as the **target variable** in classification.

---

### 🌟 Transit Parameters  
- **Fields:** `koi_period`, `koi_time`, `koi_impact`, `koi_duration`, `koi_depth`, `koi_prad`, `koi_teq`, `koi_insol`  
- **Description:** Derived from fitting models to light curves. These describe the planet’s **orbital and transit characteristics** such as:
  - **Orbital Period**  
  - **Transit Epoch**  
  - **Planet-Star Radius Ratio**  
  - **Planet–Star Distance / Star Radius**  
  - **Impact Parameter**

---

### 📡 Threshold Crossing Event (TCE) Information  
- **Fields:** `koi_model_snr`, `koi_tce_plnt_num`, `koi_tce_delivname`  
- **Description:** Kepler’s **Transiting Planet Search (TPS)** module identifies potential planetary signals by:
  - Filtering out noise
  - Applying thresholds to minimize false alarms
  - Flagging likely candidates for further validation

---

### ☀️ Stellar Parameters  
- **Fields:** `koi_steff`, `koi_slogg`, `koi_srad`  
- **Description:** Characteristics of the host star, including:
  - **Effective Temperature**
  - **Surface Gravity**
  - **Stellar Radius**

---

## 🧠 Key Insights

- **Gradient Boosting** emerged as the top-performing model with **~83.6% accuracy**.  
- **Signal-to-noise ratio** and **transit duration** were the most critical features for classification.  
- Combining stellar, transit, and signal characteristics enhances model performance.  
- Machine learning can significantly reduce manual classification efforts, improving **efficiency and accuracy** in exoplanet discovery.

---

## 🛠 Technologies & Techniques

- **Languages:** Python  
- **Libraries:** Pandas, NumPy, Scikit-learn, TensorFlow/Keras, Matplotlib, Seaborn  
- **ML Models:** Logistic Regression, KNN, SVM, Decision Tree, Random Forest, Neural Network, Gradient Boosting  
- **Evaluation Metrics:** Accuracy, Precision, Recall, F1 Score  

---

## 🌍 Potential Impact

Applying machine learning to exoplanet classification can:
- Accelerate **discovery of new worlds**
- Improve **target prioritization** for follow-up observations
- Support the **search for habitable exoplanets**
- Free astronomers from manual sifting, allowing them to focus on deeper analysis

---

