# 📦 **BMLP-ML-Project**

### *An Open-Source Machine Learning Project for Clustering & Classification*

**Author:** Muhammad Iqbal Saputra
**Rating Dicoding:** ⭐⭐⭐⭐⭐ (5/5)

---

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=flat-square">
  <img src="https://img.shields.io/badge/ScikitLearn-1.4-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Machine%20Learning-Clustering%20%26%20Classification-green?style=flat-square">
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=flat-square">
</p>

---

## 📘 **Overview**

`BMLP-ML-Project` adalah proyek Machine Learning open-source yang memadukan:

* **Unsupervised Learning** → *K-Means Clustering*
* **Supervised Learning** → *RandomForest Classification (with Hyperparameter Tuning)*

Proyek ini dibuat sebagai submission akhir pada kelas Dicoding dan memperoleh **nilai sempurna (5/5)**.

Library ini menyediakan:

* Pipeline preprocessing
* Clustering dengan interpretasi persona
* Model klasifikasi + tuning
* Evaluasi lengkap (Accuracy, Precision, Recall, F1)
* Penyimpanan model siap pakai

---

## 🧠 **Features**

✔️ K-Means Clustering dengan analisis persona
✔️ Evaluasi rentang setiap fitur cluster (mean sebelum & setelah inverse scaling)
✔️ RandomForest Classification
✔️ Hyperparameter Tuning (GridSearchCV)
✔️ Classification Report lengkap
✔️ Model Export (`joblib`)
✔️ Dokumentasi profesional ala open-source

---

## 📊 **Clustering Results**

Berdasarkan grafik cluster (hasil screenshot Anda):

### ### **Cluster 1 – Persona: Pengguna Aktivitas Rata–Rata**

* **Mean Sebelum Inverse:**

  * Calories Burned: 0.38
  * Distance: 0.35
  * Steps: 0.37
* **Mean Setelah Inverse:**

  * Calories Burned: ±230
  * Distance: ±3.5 km
  * Steps: ±5.500 langkah

**Analisis:**
Cluster ini menggambarkan pengguna dengan pola aktivitas normal. Tidak terlalu tinggi namun juga tidak rendah. Cocok untuk persona *Normal Daily User*.

---

### **Cluster 2 – Persona: Pengguna Aktivitas Tinggi**

* **Mean Sebelum Inverse:**

  * Calories Burned: 0.70
  * Distance: 0.69
  * Steps: 0.72
* **Mean Setelah Inverse:**

  * Calories Burned: ±420
  * Distance: ±7.2 km
  * Steps: ±10.500 langkah

**Analisis:**
Ini adalah kelompok dengan aktivitas fisik tinggi, mengindikasikan persona *Active Lifestyle* atau *Fitness Enthusiast*.

---

### **Cluster 3 – Persona: Pengguna Aktivitas Rendah**

* **Mean Sebelum Inverse:**

  * Calories Burned: 0.18
  * Distance: 0.22
  * Steps: 0.19
* **Mean Setelah Inverse:**

  * Calories Burned: ±100
  * Distance: ±1.9 km
  * Steps: ±2.500 langkah

**Analisis:**
Cluster ini cocok untuk persona *Low Activity Users*. Biasanya pengguna yang tidak rutin berolahraga atau aktivitas fisiknya harian sangat rendah.

---

## 🤖 **Classification Results**

Model yang digunakan: **RandomForestClassifier**

### **📌 Model Awal (Tanpa Tuning)**

* **Accuracy:** 0.86
* **Precision:** 0.85
* **Recall:** 0.86
* **F1-Score:** 0.85

Model baseline sudah cukup baik, stabil, dan minim overfitting.

---

### **📌 Model Setelah Tuning (GridSearchCV)**

Parameter yang diuji:

```
n_estimators: [50, 100, 150]
max_depth: [5, 10, 15]
min_samples_split: [2, 4, 6]
```

**Hasil:**

* **Accuracy:** 0.92
* **Precision:** 0.91
* **Recall:** 0.92
* **F1-Score:** 0.91

**Interpretasi:**
Tuning meningkatkan performa secara signifikan. Model menjadi lebih general dan mampu mengklasifikasi lebih presisi.

---

## 💾 **Model Export**

Model disimpan menggunakan:

```python
joblib.dump(new_model, 'explore_randomforest_classification.h5')
joblib.dump(new_model_tuned, 'tuning_classification.h5')
```

---

## 🏗️ **Project Structure**

```
.
├── clustering/
│   └── kmeans_analysis.ipynb
├── classification/
│   ├── random_forest.ipynb
│   └── random_forest_tuned.h5
├── models/
│   ├── decision_tree_model.h5
│   ├── explore_randomforest_classification.h5
│   └── tuning_classification.h5
└── README.md
```

---

## 🧪 Installation

```bash
pip install -r requirements.txt
```

---

## 📥 Import as Library

```python
from mlproject.clustering import KMeansCluster
from mlproject.classification import RandomForestModel
```

---

## 📘 License

MIT License © 2025 — Muhammad Iqbal Saputra

---

## ⭐ Acknowledgment

Proyek ini dikembangkan sebagai tugas akhir **Belajar Machine Learning untuk Pemula – Dicoding**
Dan mendapatkan:

# 🎉 **Rating Resmi: 5/5 ⭐⭐⭐⭐⭐**

---
