# Project-Capstone-IBM-
Trashtype Classification CNN

Baik! Berdasarkan isi proyekmu (dari file notebook dan slide yang kamu kirim sebelumnya), berikut adalah **README.md** yang sudah disesuaikan secara spesifik dengan proyek CNN klasifikasi gambar jenis sampah (dengan 6 kelas) yang kamu buat. Ini sudah disesuaikan agar *penilai tidak bingung* dan langsung paham:

---

# 🧠 CNN untuk Klasifikasi Jenis Sampah

## 📌 Deskripsi Proyek

Proyek ini merupakan implementasi model *Convolutional Neural Network* (CNN) untuk mendeteksi dan mengklasifikasi gambar sampah ke dalam 6 kategori, yaitu:

* **cardboard**
* **glass**
* **metal**
* **paper**
* **plastic**
* **trash**

Model dilatih dengan dataset gambar sampah terstruktur yang diproses menggunakan TensorFlow dan Keras, dengan tujuan membangun sistem klasifikasi gambar otomatis berbasis Deep Learning.

---

## 🗂️ Struktur Dataset

Dataset disusun dalam tiga folder utama, yaitu:

```
├── train/     → Data latih
├── val/       → Data validasi
└── test/      → Data pengujian
```

Setiap folder berisi 6 subfolder yang mewakili kelas sampah:

```
cardboard/, glass/, metal/, paper/, plastic/, trash/
```

---

## ⚙️ Teknologi dan Library

Proyek ini dibangun menggunakan:

* Python 3
* TensorFlow & Keras
* Matplotlib
* NumPy
* Google Colab (untuk eksekusi notebook)

---

## 🏗️ Arsitektur Model CNN

Struktur model CNN yang digunakan adalah sebagai berikut:

1. **Conv2D Layer** dengan 32 filter dan ReLU activation
2. **MaxPooling2D** untuk mengurangi dimensi
3. **Conv2D Layer** kedua dengan 64 filter
4. **MaxPooling2D** lagi
5. **Flatten Layer**
6. **Dense Layer** 128 unit dengan ReLU
7. **Output Dense Layer** 6 unit dengan Softmax (untuk klasifikasi multi-kelas)

Model di-*compile* dengan:

* **Loss Function**: `categorical_crossentropy`
* **Optimizer**: `adam`
* **Metric**: `accuracy`

---

## 📈 Pelatihan Model

Model dilatih selama 10 epoch dengan `batch_size=32`. Proses pelatihan menggunakan generator gambar dari direktori yang melakukan *rescaling* dan *augmentation*.

### Hasil Pelatihan:

* **Akurasi Pelatihan**: \~99%
* **Akurasi Validasi**: \~96%
* Model menunjukkan **tidak overfitting**, ditunjukkan dengan grafik `loss` dan `accuracy` yang seimbang antara data latih dan validasi.

---

## 🧪 Evaluasi Model

Model diuji menggunakan data `test/` dan dievaluasi berdasarkan:

* **Akurasi Prediksi**
* **Confusion Matrix**
* **Laporan Klasifikasi (`classification_report`)**
* Visualisasi hasil prediksi acak untuk 10 gambar dari data uji.

---

## 💡 Kesimpulan

Model CNN yang dibangun berhasil melakukan klasifikasi gambar sampah ke dalam 6 kategori dengan akurasi tinggi dan generalisasi yang baik. Proyek ini menunjukkan bahwa teknologi deep learning dapat dimanfaatkan untuk mendukung pengelolaan sampah berbasis teknologi secara lebih efisien.

---

## 📚 Referensi

* Dokumentasi [TensorFlow](https://www.tensorflow.org/)
* Tutorial CNN Keras: [https://keras.io/examples/vision/image\_classification\_from\_scratch/](https://keras.io/examples/vision/image_classification_from_scratch/)
* Dataset: https://www.kaggle.com/datasets/farzadnekouei/trash-type-image-dataset
---

Kalau kamu butuh README-nya dalam bentuk file `.md`, aku bisa bantu generate juga. Mau?
