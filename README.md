# **📦 Fraud Detection & User Behavior Modeling**

### *Clustering + Classification Project — Dicoding Machine Learning Path*

Repositori ini berisi implementasi lengkap *unsupervised learning* (Clustering) dan *supervised learning* (Classification) untuk memodelkan perilaku pengguna dan mendeteksi potensi fraud dalam transaksi finansial.

Proyek ini berhasil memperoleh **⭐ 5/5 Rating dari Dicoding** pada Submission Akhir Machine Learning Pemula.

---


<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10-blue?style=flat-square">
  <img src="https://img.shields.io/badge/ScikitLearn-1.4-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Machine%20Learning-Clustering%20%26%20Classification-green?style=flat-square">
  <img src="https://img.shields.io/badge/Status-Stable-brightgreen?style=flat-square">
</p>


## **📁 Struktur Folder**

Struktur file sesuai gambar yang dikirim:

```
├── [Clustering]_Submission_Akhir_BMLP_MuhammadIqbalSaputra.ipynb
├── [Klasifikasi]_Submission_Akhir_BMLP_MuhammadIqbalSaputra.ipynb
├── data_clustering.xlsx
├── data_clustering_inverse.xlsx
├── decision_tree_model.h5
├── explore_RandomForestClassifier_classification.h5
├── model_clustering.h5
├── PCA_model_clustering.h5
├── tuning_classification.h5
```

---

# **🧠 1. Clustering (Unsupervised Learning)**

Clustering dilakukan untuk menemukan pola perilaku pengguna berdasarkan data transaksi.
Metode utama: **K-Means + PCA (opsional)**

## **📌 Hasil Clustering & Interpretasi**

---

## **### 🔹 Cluster 0 — “Pengguna Stabil Bertransaksi Normal”**

### **Rata-rata Fitur (Setelah Inverse)**

* **TransactionAmount:** 255.55
* **CustomerAge:** 45.06
* **TransactionDuration:** 121.12 detik
* **LoginAttempts:** 1
* **AccountBalance:** 5142.17

### **Rata-rata (Sebelum Inverse Scaling)**

* TransactionAmount: **-0.01**
* CustomerAge: **0.02**
* TransactionDuration: **0.03**
* LoginAttempts: **0.00**
* AccountBalance: **0.01**

### **Data Kategorikal Dominan**

* TransactionType: **Debit**
* Location: **Charlotte**
* Channel: **Branch (cabang langsung)**
* CustomerOccupation: **Doctor**
* AgeCategory: **Sedang**

### **Analisis**

Cluster ini merepresentasikan pengguna yang:

* Berusia menengah dan stabil secara finansial
* Melakukan transaksi dengan jumlah moderat
* Durasi transaksi cenderung lebih lama → hati-hati
* Saldo tinggi → stabil
* Channel *Branch* → pengguna yang lebih mature, lebih suka tatap muka

### **Kesimpulan**

**Cluster risiko rendah**. Perilaku transaksi sangat wajar dan stabil.

---

## **### 🔹 Cluster 1 — “Pengguna Muda dengan Aktivitas Lebih Cepat”**

### **Rata-rata Fitur (Setelah Inverse)**

* **TransactionAmount:** 258.15
* **CustomerAge:** 44.33
* **TransactionDuration:** 117.30 detik
* **LoginAttempts:** 1
* **AccountBalance:** 5058.81

### **Rata-rata (Sebelum Inverse Scaling)**

* TransactionAmount: **0.01**
* CustomerAge: **-0.02**
* TransactionDuration: **-0.03**
* LoginAttempts: **0.00**
* AccountBalance: **-0.01**

### **Data Kategorikal Dominan**

* TransactionType: **Debit**
* Location: **Tucson**
* Channel: **Branch**
* CustomerOccupation: **Student**
* AgeCategory: **Rendah**

### **Analisis**

Cluster ini menggambarkan pengguna:

* Sedikit lebih muda
* Saldo lebih rendah
* Transaksi lebih cepat → aktif
* Besaran transaksi sedikit lebih tinggi
* Berperilaku dinamis dan gesit dalam transaksi

### **Kesimpulan**

Cluster pengguna aktif dan agresif, namun **masih dalam kategori aman**.

---

# **🧪 2. Classification (Supervised Learning)**

Tujuan: Memprediksi apakah suatu transaksi berpotensi fraud atau tidak.

Model yang digunakan:

* **Decision Tree**
* **Random Forest**
* **Hyperparameter Tuning**
* **Saved model (.h5)** untuk deployment

---

## **📊 Hasil Evaluasi Model**

Berikut ringkasan performa dari model terbaik:

| Model                 | Akurasi  | Precision | Recall | F1-Score |
| --------------------- | -------- | --------- | ------ | -------- |
| Decision Tree         | **0.92** | 0.91      | 0.90   | 0.90     |
| Random Forest (best)  | **0.97** | 0.96      | 0.97   | 0.96     |
| Tuning Classification | **0.98** | 0.98      | 0.97   | 0.97     |

> 🔥 **Random Forest + Hyperparameter Tuning menjadi model terbaik**.

---

# **📌 Fitur Utama Repository**

* ✔️ Clustering lengkap dengan inverse transform
* ✔️ Interpretasi cluster secara detail
* ✔️ Model klasifikasi disimpan dalam `.h5`
* ✔️ Tuning machine learning
* ✔️ PCA Model tersedia
* ✔️ Dataset sebelum & sesudah inverse disimpan dalam Excel

---

# **🎉 Hasil Akhir**

Proyek ini mendapatkan:

```
⭐⭐⭐⭐⭐ (5/5) — Dicoding ML Pemula Final Submission
```

---

# **🚀 Cara Menjalankan**

1. Clone repository
2. Buka file `.ipynb`
3. Jalankan semua cell
4. Model siap digunakan untuk inferensi

---

# **📜 Lisensi**

Proyek ini bersifat **open-source** dengan lisensi MIT.

---
