# 🏠 Prediksi Harga Rumah Berdasarkan Kemiripan Atribut

Proyek ini bertujuan untuk memprediksi harga rumah berdasarkan atribut seperti **luas tanah**, **luas bangunan**, dan **jarak ke pusat kota** menggunakan metode kemiripan atribut sederhana (nearest neighbor).

---

## 🎯 Tujuan Proyek

- Mengambil dan memproses data harga rumah dari sumber online.  
- Melakukan normalisasi atribut numerik agar skala atribut seragam.  
- Membangun sistem prediksi harga rumah berdasarkan nilai kemiripan atribut input dengan data yang sudah ada.  

---

## 🛠️ Teknologi dan Library yang Digunakan

- **Bahasa Pemrograman:** Python  
- **Library Utama:**  
  - `requests` — Mengunduh data dari URL  
  - `csv` — Memproses data CSV  
  - `contextlib` — Mengelola resource koneksi HTTP  

---

## 🚀 Alur Proyek

1. **Pengambilan Data**  
  - Mengunduh dan membaca file `harga_rumah.txt` dari URL yang disediakan.  
  - Mengonversi data menjadi list of dictionary untuk kemudahan akses.  

2. **Normalisasi Data**  
  - Menghitung nilai minimum dan maksimum untuk atribut: `tanah`, `bangunan`, dan `jarak_ke_pusat`.  
  - Melakukan transformasi atribut ke skala 0-1 menggunakan normalisasi min-max.  

3. **Transformasi Data Baru**  
  - Mengaplikasikan normalisasi pada data input baru berdasarkan info atribut yang sudah dihitung.  

4. **Prediksi Harga**  
  - Menghitung kemiripan (berdasarkan selisih absolut) antara data input dan dataset.  
  - Memilih harga rumah dari data yang paling mirip sebagai prediksi.  

---

## 📦 Instalasi

Sebelum menjalankan skrip, pastikan library `requests` sudah terinstal.  
Jalankan perintah berikut pada terminal Anda:  

pip install requests

---

## 📈 Contoh Penggunaan

data = {'tanah': 110, 'bangunan': 80, 'jarak_ke_pusat': 35}  
data = transform_data(data, attr_info)  
harga = price_based_on_similarity(data, harga_rumah)  
print("Prediksi harga rumah: ", harga)

---

## 📂 Dataset

- **Sumber Data:**  
  https://storage.googleapis.com/dqlab-dataset/harga_rumah.txt  
- **Atribut yang Digunakan:**  
  `tanah`, `bangunan`, `jarak_ke_pusat`, `harga`

---

## ✅ Output Akhir

Prediksi harga rumah berdasarkan kemiripan atribut input dengan data yang sudah dinormalisasi.

---

## 🔍 Catatan

- Data diambil langsung dari URL dan diproses secara dinamis saat runtime.  
- Pendekatan ini menggunakan perhitungan kemiripan sederhana dan bisa dikembangkan dengan metode machine learning lain.  

---

## ⚠️ Lisensi dan Hak Cipta

- Dataset milik **DQLab Academy** dan digunakan hanya untuk keperluan edukasi.  
- Mohon tidak disebarluaskan atau digunakan di luar konteks pembelajaran tanpa izin.  

---

## 👨‍💻 Tentang Pengembang

**Yoga Pratama**  
Email: yp170090@gmail.com  
LinkedIn: https://linkedin.com/in/yoga-pratama-923202349  
GitHub: https://github.com/Yongsjasjos  

---
