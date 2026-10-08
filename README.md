# Prediksi Konsentrasi PM2.5 Menggunakan Random Forest

## 1. Deskripsi

Project ini merupakan studi kasus penerapan **Machine Learning** untuk memprediksi konsentrasi **PM2.5** berdasarkan data meteorologi.

Studi kasus ini dibuat sebagai implementasi materi **High Performance Computing (HPC)** dengan menghubungkan permasalahan lingkungan, data, Machine Learning, dan pengembangan komputasi.

Dataset yang digunakan adalah **Beijing PM2.5 Dataset** dari Kaggle.

---

## 2. Tujuan

Tujuan dari project ini adalah:

1. Menganalisis data konsentrasi PM2.5.
2. Melakukan preprocessing terhadap dataset.
3. Membuat model Machine Learning menggunakan Random Forest.
4. Memprediksi konsentrasi PM2.5.
5. Mengevaluasi performa model.
6. Mengetahui fitur yang paling berpengaruh terhadap prediksi.
7. Menunjukkan pengembangan studi kasus menuju sistem berbasis HPC.

---

## 3. Dataset

Dataset yang digunakan:

**Beijing PM2.5 Dataset**

Dataset berisi data kualitas udara dan kondisi meteorologi secara berkala.

Beberapa variabel yang digunakan:

* `year` — tahun
* `month` — bulan
* `day` — hari
* `hour` — jam
* `DEWP` — dew point
* `TEMP` — temperatur
* `PRES` — tekanan udara
* `cbwd` — arah angin
* `Iws` — kecepatan angin
* `Is` — akumulasi salju
* `Ir` — akumulasi hujan
* `pm2.5` — konsentrasi PM2.5

Variabel `pm2.5` digunakan sebagai **target prediksi**.

---

## 4. Metode

Metode Machine Learning yang digunakan adalah:

**Random Forest Regressor**

Tahapan penelitian:

```text
Dataset Kaggle
      ↓
Data Preprocessing
      ↓
Exploratory Data Analysis
      ↓
Feature Selection
      ↓
Train-Test Split
      ↓
Random Forest
      ↓
Prediksi PM2.5
      ↓
Evaluasi Model
      ↓
Feature Importance
```

---

## 5. Preprocessing

Tahapan preprocessing yang dilakukan meliputi:

* Membaca dataset.
* Membuat kolom waktu (`datetime`).
* Menangani missing value.
* Mengisi missing value pada fitur numerik menggunakan median.
* Mengisi missing value arah angin menggunakan nilai modus.
* Melakukan One-Hot Encoding pada variabel arah angin.

---

## 6. Evaluasi Model

Performa model dievaluasi menggunakan:

### MAE

**Mean Absolute Error (MAE)** digunakan untuk mengetahui rata-rata kesalahan prediksi.

### RMSE

**Root Mean Squared Error (RMSE)** digunakan untuk mengukur besarnya kesalahan prediksi dengan memberikan penalti lebih besar terhadap error yang besar.

### R² Score

**R² Score** digunakan untuk melihat seberapa baik model menjelaskan variasi pada data target.

Hasil evaluasi dapat dilihat setelah notebook dijalankan.

---

## 7. Hasil

Model menghasilkan prediksi konsentrasi PM2.5 berdasarkan kondisi meteorologi.

Selain melakukan prediksi, project ini juga menggunakan **Feature Importance** untuk mengetahui fitur yang paling berpengaruh terhadap model Random Forest.

Hasil tersebut dapat digunakan sebagai dasar untuk melakukan analisis lebih lanjut terhadap faktor yang berhubungan dengan konsentrasi PM2.5.

---

## 8. Teknologi yang Digunakan

Project ini menggunakan:

* Python
* Google Colab
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib
* GitHub

---

## 9. Hubungan dengan HPC

Studi kasus ini dapat dikembangkan menjadi sistem High Performance Computing (HPC).

Pengembangan yang dapat dilakukan antara lain:

* Menggunakan dataset kualitas udara dalam jumlah besar.
* Menggunakan data dari banyak sensor IoT.
* Melakukan preprocessing secara paralel.
* Menggunakan GPU untuk proses Machine Learning.
* Menjalankan beberapa eksperimen model secara bersamaan.
* Menggunakan cloud computing atau HPC cluster.
* Membuat sistem monitoring PM2.5 secara real-time.

Konsep pengembangannya:

```text
Sensor IoT
    ↓
Pengumpulan Data
    ↓
Data Processing
    ↓
HPC / GPU
    ↓
Machine Learning
    ↓
Prediksi PM2.5
    ↓
Dashboard
```

---

## 10. Struktur Repository

```text
prediksi-pm25-random-forest/
│
├── README.md
│
└── Studi_Kasus_PM25_Random_Forest.ipynb
```

File notebook berisi seluruh proses mulai dari preprocessing dataset hingga evaluasi model.

---

## 11. Kesimpulan

Project ini menunjukkan penerapan Machine Learning untuk menyelesaikan permasalahan kualitas udara menggunakan data PM2.5.

Random Forest digunakan untuk mempelajari hubungan antara kondisi meteorologi dengan konsentrasi PM2.5.

Studi kasus ini juga dapat dikembangkan lebih lanjut dengan integrasi **IoT, GPU, cloud computing, dan HPC** sehingga dapat digunakan untuk sistem monitoring dan prediksi kualitas udara secara lebih besar dan real-time.
