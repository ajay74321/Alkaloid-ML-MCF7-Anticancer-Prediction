# Alkaloid-ML-MCF7-Anticancer-Prediction
A machine learning project developed to predict the anticancer potency of alkaloid compounds against MCF-7 breast cancer cells. The workflow includes data extraction, preprocessing, molecular descriptor generation, feature engineering, model training, and performance evaluation to identify the most reliable predictive model for alkaloid activity


# **Determination of Anti-Cancer Potency of Alkaloids Against MCF-7 Breast Cancer Cells Using Machine Learning**

*Based on project slides* 

---

## 🔰 **Shields.io Badges**

<p>
  <img src="https://img.shields.io/badge/Python-ML-blue" />
  <img src="https://img.shields.io/badge/ScikitLearn-Modeling-orange" />
  <img src="https://img.shields.io/badge/CancerCellLine-MCF7-red" />
  <img src="https://img.shields.io/badge/Data-Alkaloids-green" />
  <img src="https://img.shields.io/badge/Status-Completed-brightgreen" />
</p>

---

## 🧬 **Project Objective**

To develop a machine learning model capable of predicting the **anti-cancer potency of alkaloid compounds** against **MCF-7 breast cancer cell lines** using bioactivity data, molecular descriptors, and structural fingerprints. 

---

## 📚 **Introduction**

Alkaloids are nitrogen-containing secondary metabolites widely found in plants and known for diverse pharmacological effects — including strong **anticancer, antimicrobial, anti-inflammatory, analgesic, antiviral**, and more.
Structurally, they contain at least one basic nitrogen atom within a heterocyclic ring, contributing to their high bioactivity. 

**Anticancer Activities of Alkaloids**

* Induce apoptosis and arrest the cell cycle
* Show cytotoxicity against **MCF-7** breast cancer cells
* Activate caspases, downregulate Bcl-2, upregulate Bax
* Inhibit PI3K/Akt/mTOR & NF-κB pathways
* Disrupt microtubule formation and DNA topoisomerase activity 

---

## 🧪 **Workflow Overview**

A structured computational pipeline was used to clean, prepare, and model alkaloid bioactivity data.

---

## 📥 **1. Data Extraction**

* Extracted alkaloid Compound IDs from the **NPASS** database
* Retrieved IC50 bioactivity values from **PubChem**
* Filtered data specifically for **MCF-7** cell line activity
* Removed empty/incomplete entries to obtain the final dataset 

---

## 🧹 **2. Data Preprocessing**

* Cleaned and filtered data
* Converted **IC50 → pIC50** using:

  ```
  pIC50 = –log10(IC50 in M)
  ```
* pIC50 improves uniformity and distribution
* Generated SDF files from PubChem for descriptor calculation 

---

## 🧬 **3. Feature Generation**

* Extracted **PubChem fingerprints**
* Extracted **2D molecular descriptors** using **PaDeL-Descriptor**
* Combined structural features for ML-ready datasets 

---

## 🤖 **4. Model Training**

Machine learning models were trained using:

* Fingerprints
* 2D descriptors
* Combined fingerprint + descriptor features

Workflow included:

* Data splitting
* Hyperparameter tuning
* Model comparison based on statistical performance metrics 

---

## 📊 **5. Model Evaluation Metrics**

Models were evaluated using:

* **Accuracy**
* **R² (Coefficient of Determination)**
* **RMSE**
* **MAPE**
* **MDAPE** 

---

## 📊 Sample Result Table

| Model                       | Features Used     | R² Score | RMSE | MAPE  | MDAPE |
| --------------------------- | ----------------- | -------- | ---- | ----- | ----- |
| Gradient Boosting Regressor | 2D Descriptors    | **0.58** | 0.70 | 9.67% | 6.64% |
| Random Forest Regressor     | Fingerprints + 2D | 0.51     | 0.75 | 11.2% | 8.90% |
| SVR                         | 2D Descriptors    | 0.47     | 0.79 | 12.8% | 9.40% |
| Linear Regression           | 2D Descriptors    | 0.29     | 0.92 | 18.5% | 15.2% |

---


