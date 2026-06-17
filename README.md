# 🌾 Predictive Modeling for Agriculture
[![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Latest-orange.svg)](https://scikit-learn.org/)
[![ML](https://img.shields.io/badge/Task-Feature%20Selection-purple.svg)](#)

## 📝 Project Description

A farmer reached out to me as a machine learning expert seeking help to select the best crop for his field. Due to budget constraints, the farmer explained that he could only afford to measure **one** out of the four essential soil measures:
* **Nitrogen** content ratio in the soil
* **Phosphorous** content ratio in the soil
* **Potassium** content ratio in the soil
* **pH** value of the soil

This is a classic **feature selection problem**: the goal is to identify which single soil metric carries the most predictive signal for the crop label, in a **22-class** classification setting.

---

## 📊 Key Findings

Logistic Regression trained on **one feature at a time** (22-class crop label), ranked by macro F1-score:

| Soil metric | F1-score (single feature) |
|-------------|---------------------------|
| **Potassium (K)** | **0.2576** ← best |
| Phosphorous (P) | 0.1003 |
| Nitrogen (N) | 0.0934 |
| pH | 0.0430 |

* **Best Predictor:** **Potassium (K)** is the most informative single metric (F1 = 0.257). On a **22-class** problem a uniform random guess scores ~0.045, so K alone reaches **~5.7×** that baseline — and roughly **2.5×** the next-best feature (P). The low absolute value is expected: no single soil reading can separate 22 crops on its own.
* **Recommendation:** If the farmer can only afford one test, measuring Potassium maximizes predictive value per euro spent.

---

## 🛠️ Technologies
* **Python** (Pandas, NumPy)
* **Scikit-Learn** (Logistic Regression, Multi-class classification, Feature Selection)

---

## 🚀 How to use
1. Clone the repository.
2. Ensure you have the `soil_measures.csv` file in the root directory.
3. Run the Jupyter Notebook `notebook.ipynb`.

---

## 👤 Contact
**Jaime Novillo Benito**
* 🔗 [LinkedIn Profile](https://www.linkedin.com/in/jaime-novillo-benito)
* 📧 [jaimenovillobenito.job@gmail.com](mailto:jaimenovillobenito.job@gmail.com)
