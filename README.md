# 🚗 Analisis Faktor Kecelakaan Lalu Lintas untuk Optimalisasi Keselamatan Jalan

**Dataset**: [Road Traffic Accidents - Kaggle](https://colab.research.google.com/drive/1-eHZaRIoiqGl-W9MCysAs4Rmhkpi2ql_#scrollTo=pfO8j_u8n9NW)

---

## 📖 Deskripsi

Proyek ini bertujuan untuk menganalisis faktor penyebab kecelakaan lalu lintas guna meningkatkan keselamatan di jalan. Berdasarkan data dari **Korlantas Polri**, pada tahun 2022 terjadi 94.617 kasus kecelakaan di Indonesia, di mana sebagian besar disebabkan oleh kesalahan manusia (human error) dengan persentase 61%. Data yang digunakan dalam penelitian ini adalah dataset kecelakaan lalu lintas yang mencakup 12.316 kejadian di Sub-Kota Addis Ababa dan terdiri dari 32 fitur.

---

## 📂 Struktur Dataset

Dataset ini mencakup berbagai informasi tentang kecelakaan lalu lintas, termasuk fitur yang relevan seperti usia pengemudi, tingkat pendidikan, waktu kecelakaan, kondisi jalan, dan lainnya. Target klasifikasi mencakup tiga kategori cedera:

- **Slight Injury**: Cedera ringan
- **Serious Injury**: Cedera berat
- **Fatal Injury**: Kecelakaan dengan korban jiwa

---

## 🔍 Metodologi

1. **Preprocessing Data**  
   - *Data Cleaning*: Menghapus nilai yang hilang atau tidak relevan.
   - *Data Reduction*: Menggunakan feature selection untuk mengurangi jumlah fitur yang digunakan dalam model.
   - *Data Transformation*: Mengonversi data kategorik menjadi numerik.
   - *Data Normalization*: Menerapkan skala Min-Max pada data numerik agar bernilai antara 0 hingga 1.

2. **Algoritma Klasifikasi**  
   Model utama yang digunakan dalam analisis ini adalah **Gradient Boosting Classifier**, yang terbukti memberikan akurasi tinggi. Selain itu, percobaan dilakukan dengan lima algoritma lainnya untuk memastikan keakuratan model.

3. **Oversampling & Balancing**  
   Menggunakan teknik **SMOTEENN** untuk menangani ketidakseimbangan kelas dalam data, yang meningkatkan akurasi prediksi model.

---

## 🎯 Hasil Analisis

- **Model Akurasi**: Model Gradient Boosting dengan Hyperparameter Tuning menunjukkan akurasi sebesar 81%.
- **Feature Importance**: Fitur `Age_band_of_driver` (kelompok umur pengemudi) dan `Educational_level` (tingkat pendidikan) menunjukkan pengaruh yang signifikan dalam menentukan tingkat keparahan kecelakaan.
- **Confusion Matrix**:
  - *Kelas 0 (Ringan)*: Mengalami kesulitan dalam mengidentifikasi kasus dengan tepat.
  - *Kelas 1 (Sedang)*: Hanya 15 dari 284 kasus diprediksi dengan benar.
  - *Kelas 2 (Fatal)*: Model berhasil memprediksi 1.613 dari 2.018 kasus dengan benar.

---

## 📈 Visualisasi Hasil

Hasil analisis disajikan dalam bentuk Confusion Matrix dan grafik yang menunjukkan pentingnya fitur. Grafik ini memberikan wawasan tentang fitur mana yang memiliki pengaruh besar terhadap prediksi kecelakaan.

---

## 🚀 Cara Menggunakan

1. Unduh dataset dari [Kaggle](https://colab.research.google.com/drive/1-eHZaRIoiqGl-W9MCysAs4Rmhkpi2ql_#scrollTo=pfO8j_u8n9NW).
2. Jalankan skrip analisis yang tersedia di repositori ini.
3. Interpretasikan hasil untuk memahami faktor utama penyebab kecelakaan lalu lintas.

---

## 📝 Kesimpulan

Hasil analisis menunjukkan bahwa **human error**, khususnya yang terkait dengan usia dan tingkat pendidikan pengemudi, merupakan faktor dominan dalam kecelakaan lalu lintas. Analisis ini diharapkan dapat membantu pihak berwenang dan masyarakat dalam merancang strategi untuk meningkatkan keselamatan di jalan.

--- 
