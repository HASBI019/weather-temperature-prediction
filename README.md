# 🌤️ Prediksi Suhu Harian Berdasarkan Data Cuaca

Proyek ini merupakan implementasi sederhana dari proses **Data Science berdasarkan standar SKKNI** (Standar Kompetensi Kerja Nasional Indonesia).  
Studi kasus yang digunakan adalah **prediksi suhu harian berdasarkan variabel cuaca** seperti kelembapan, tekanan udara, dan kecepatan angin.

---

## 🎯 Tujuan Proyek
- Memprediksi suhu (temperature) berdasarkan data cuaca.
- Mempelajari tahapan Data Science dari **Business Understanding** hingga **Modeling**.
- Menggunakan algoritma **Linear Regression** untuk prediksi suhu.

---

## 🧠 Tahapan Data Science (SKKNI)

### 1️⃣ Business Understanding
Instansi cuaca ingin memahami bagaimana variabel cuaca seperti kelembapan, tekanan udara, dan kecepatan angin memengaruhi suhu harian.

### 2️⃣ Data Understanding
- Dataset: `weatherHistory.csv` (96.453 baris, 12 kolom)
- Kolom penting: `Temperature (C)`, `Humidity`, `Wind Speed (km/h)`, `Pressure (millibars)`
- Missing values: 517 pada kolom `Precip Type`
- Rata-rata suhu: **11.93°C**
- Suhu maksimum: **39.90°C**
- Suhu minimum: **-21.82°C**

### 3️⃣ Data Preparation
Langkah pembersihan data:
- Menghapus kolom yang tidak relevan (`Daily Summary`, `Loud Cover`)
- Menghapus baris kosong pada `Precip Type`
- Mengubah format tanggal dan menstandarkan nama kolom

### 4️⃣ Modeling
Model yang digunakan: **Linear Regression**

Variabel input (X):
- `Humidity`
- `wind_speed`
- `pressure`

Target (y):
- `temperature`

### 5️⃣ Evaluation
Hasil evaluasi model:
- **Mean Absolute Error (MAE):** 5.87  
- **R-squared (R²):** 0.42  

Artinya model sudah mampu memprediksi suhu dengan cukup baik berdasarkan variabel cuaca.

---

## 📊 Visualisasi
- Distribusi suhu (`plt.hist(df['temperature'])`)
- Perbandingan suhu asli dan prediksi (`plt.scatter(y_test, y_pred)`)

---

## 🧰 Tools & Library
Proyek ini dijalankan menggunakan:
- Python 3 (Google Colab)
- Pandas
- Matplotlib
- Scikit-learn

---

## 📁 Struktur File
