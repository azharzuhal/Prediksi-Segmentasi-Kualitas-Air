# Prediksi-Segmentasi-Kualitas-Air
Analisis kualitas air menggunakan Machine Learning: Klasifikasi kelayakan air minum dengan Regresi Logistik (Akurasi 60.98%) dan pemetaan karakteristik kontaminan air menggunakan K-Means Clustering (3 Profil Cluster). Dikembangkan secara lokal dengan Python, Pandas, dan Scikit-Learn di VS Code.

# 🚰 Analisis Kualitas Air: Prediksi Potabilitas & Segmentasi Profil

Proyek ini berfokus pada pemanfaatan teknik *Machine Learning* untuk menganalisis data kualitas air dari dua pendekatan: pembelajaran diawasi (*supervised learning*) untuk memprediksi kelayakan air minum, serta pembelajaran tidak diawasi (*unsupervised learning*) untuk mengelompokkan karakteristik kontaminan sampel air.

---

## 📊 Deskripsi Proyek & Hasil Analisis

### 1. Prediksi Potabilitas Air (Supervised Learning)
* **Berkas Kode:** `Prediksi_Kualitas_Air.ipynb`
* **Algoritma:** Regresi Logistik (*Logistic Regression*)
* **Tujuan:** Memprediksi apakah sampel air layak dikonsumsi (*potable*) atau tidak layak berdasarkan parameter kimiawi yang terukur.
* **Poin Hasil Analisis:**
  * Model berhasil memberikan tingkat akurasi pengujian sebesar **60.98%** dalam mengklasifikasikan kelayakan air.
  * Berdasarkan nilai koefisien model, fitur **`Solids`** memiliki pengaruh positif terbesar (semakin tinggi nilainya, kecenderungan air dinilai layak minum meningkat).
  * Fitur **`Organic_carbon`** memiliki pengaruh negatif terbesar (semakin tinggi kandungan karbon organik, probabilitas air layak minum menurun secara signifikan).

### 2. Segmentasi Profil Kualitas Air (Unsupervised Learning)
* **Berkas Kode:** `Segmentasi_Profil_Kualitas_Air.ipynb`
* **Algoritma:** K-Means Clustering
* **Tujuan:** Mengelompokkan karakteristik zat kimia dan fisik air ke dalam beberapa profil (klaster) tanpa menggunakan label target awal.
* **Poin Hasil Analisis:**
  * Analisis berhasil mengidentifikasi **3 Profil Cluster** unik dari sebaran data:
  * **Cluster 0 & 1:** Memiliki karakteristik kandungan unsur kimia yang cenderung seimbang dengan variasi normal pada zat terlarut.
  * **Cluster 2:** Memiliki karakteristik air dengan kandungan sangat tinggi pada komponen *Hardness* (kesadahan), *Sulfate*, dan *Organic_carbon*, namun memiliki nilai yang cukup rendah pada aspek *Solids* serta *Conductivity*.

---

## 🛠️ Tech Stack & Libraries
* **Bahasa Pemrograman:** Python
* **Environment:** VS Code (Jupyter Extension) / Google Colab
* **Libraries Utama:**
  * `Pandas` & `NumPy` (Eksplorasi, Manipulasi, dan Pembersihan Data)
  * `Matplotlib` & `Seaborn` (Visualisasi Data & Grafik Distribusi)
  * `Scikit-Learn` (Pemisahan Data, Pemodelan Regresi Logistik, & Klasterisasi K-Means)

---

🚀 Cara Menjalankan Proyek Secara Lokal
Jika Anda ingin menjalankan atau mengembangkan proyek ini di komputer lokal menggunakan VS Code, ikuti langkah-langkah di bawah ini:

1. Persiapan Berkas
Pastikan file dataset water_potability.csv diletakkan di dalam folder direktori yang sama dengan kedua file .ipynb agar kode pembacaan data (pd.read_csv) tidak mengalami error FileNotFoundError.

2. Instalasi Library Dependensi
Buka VS Code, pastikan ekstensi Jupyter dari Microsoft sudah terpasang, lalu jalankan perintah instalasi library berikut melalui Terminal lokal Anda:

Bash
pip install pandas numpy scikit-learn matplotlib seaborn jupyter
3. Eksekusi Program
Buka salah satu file .ipynb di VS Code.

Klik tombol Select Kernel di pojok kanan atas layar, lalu pilih lingkungan (environment) Python lokal komputer Anda.

Klik Run All atau jalankan setiap kotak kode (cell) secara berurutan dari atas ke bawah.

Proyek ini diselesaikan sebagai bagian dari luaran tugas akademik bidang Machine Learning / Data Science pada Program Studi Informatika Universitas Islam Indonesia.

---

## 📂 Struktur Repositori

```plaintext
├── water_potability.csv                 # Dataset Utama Kualitas Air
├── Prediksi_Kualitas_Air.ipynb          # Notebook Model Prediksi
├── Segmentasi_Profil_Kualitas_Air.ipynb # Notebook Model Klasterisasi
└── README.md                            # Dokumentasi Utama Proyek
