# Klasifikasi Aksara Kaganga Menggunakan Convolutional Neural Network (CNN)

## Kelompok 12

Program Studi Informatika  
Fakultas Teknik  
Universitas Bengkulu

---

## Anggota Kelompok 12

| No | Nama | NPM |
|----|------|-----|
| 1 | Reyhan Maulana Ibrahim | G1A023046 |
| 2 | Yovanza Villareal | G1A023054 |
| 3 | Revialdi Rifki Ramadhan Permana | G1A023066 |

---

## Deskripsi Proyek

Proyek ini bertujuan untuk membangun sistem klasifikasi citra Aksara Kaganga menggunakan metode **Convolutional Neural Network (CNN)**. Sistem dirancang untuk mengenali karakter aksara berdasarkan gambar yang diberikan dan mengelompokkannya ke dalam kelas yang sesuai.

Aksara Kaganga merupakan salah satu aksara tradisional yang digunakan di wilayah Bengkulu dan sekitarnya. Dengan memanfaatkan teknologi Deep Learning, proses pengenalan karakter dapat dilakukan secara otomatis dengan tingkat akurasi yang baik.

---

## Tujuan

- Mempelajari penerapan Deep Learning dalam pengolahan citra.
- Mengimplementasikan algoritma CNN untuk klasifikasi Aksara Kaganga.
- Melatih model agar mampu mengenali pola karakter aksara.
- Mengevaluasi performa model menggunakan data pengujian.

---

## Teknologi yang Digunakan

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab / Jupyter Notebook

---

## Struktur Repository

```text
.
├── dataset/
│   ├── train/
│   └── validation/
├── model_kaganga.keras
├── Untitled1.ipynb
└── README.md
```

---

## Penjelasan Sistem

Sistem klasifikasi Aksara Kaganga dibangun menggunakan metode Convolutional Neural Network (CNN). CNN dipilih karena memiliki kemampuan yang sangat baik dalam mengenali pola visual pada gambar.

### 1. Input Data

Dataset yang digunakan berupa kumpulan gambar karakter Aksara Kaganga yang telah dikelompokkan berdasarkan kelas masing-masing.

Setiap gambar akan diproses dan diubah ukurannya menjadi **64 × 64 piksel** agar sesuai dengan kebutuhan model CNN.

### 2. Preprocessing dan Data Augmentation

Sebelum proses pelatihan dilakukan, data terlebih dahulu diproses menggunakan teknik **Data Augmentation** untuk meningkatkan variasi data dan mengurangi risiko overfitting.

Teknik yang digunakan antara lain:

- Rescaling (1/255)
- Rotation Range = 10°
- Zoom Range = 0.1
- Width Shift Range = 0.1
- Height Shift Range = 0.1

Tahap ini membantu model belajar dari berbagai variasi bentuk karakter.

### 3. Pelatihan Model CNN

Model CNN terdiri dari beberapa lapisan:

- Convolution Layer
- Max Pooling Layer
- Flatten Layer
- Dense Layer
- Output Layer (Softmax)

Convolution Layer berfungsi mengekstraksi fitur penting dari gambar, sedangkan Max Pooling digunakan untuk mengurangi dimensi data tanpa kehilangan informasi utama.

Setelah fitur diperoleh, data akan diratakan menggunakan Flatten Layer dan diteruskan ke Dense Layer untuk proses klasifikasi.

### 4. Proses Klasifikasi

Pada tahap ini model akan memprediksi kelas aksara berdasarkan fitur yang telah dipelajari selama proses training.

Output akhir menggunakan fungsi aktivasi **Softmax** sehingga menghasilkan probabilitas untuk setiap kelas aksara.

### 5. Evaluasi Model

Kinerja model dievaluasi menggunakan:

- Training Accuracy
- Validation Accuracy
- Training Loss
- Validation Loss
- Confusion Matrix

Hasil evaluasi digunakan untuk mengetahui seberapa baik model dalam mengenali karakter Aksara Kaganga.

---

## Arsitektur CNN

Model CNN yang digunakan memiliki struktur sebagai berikut:

1. Input Layer (64 × 64 × 3)
2. Convolution Layer (32 Filter)
3. Max Pooling Layer
4. Convolution Layer (64 Filter)
5. Max Pooling Layer
6. Convolution Layer (128 Filter)
7. Max Pooling Layer
8. Flatten Layer
9. Dense Layer
10. Output Layer (Softmax)

---

## Parameter Pelatihan

| Parameter | Nilai |
|------------|--------|
| Epoch | 15 |
| Batch Size | 32 |
| Optimizer | Adam |
| Loss Function | Categorical Crossentropy |

---

## Alur Kerja Sistem

```text
Dataset Gambar
       │
       ▼
Preprocessing
(Data Augmentation)
       │
       ▼
Training CNN
       │
       ▼
Model Terlatih
       │
       ▼
Prediksi Karakter
       │
       ▼
Evaluasi Model
```

---

## Cara Menjalankan Program

### 1. Clone Repository

```bash
git clone https://github.com/username/repository.git
```

### 2. Install Dependency

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

### 3. Jalankan Notebook

```bash
jupyter notebook Untitled1.ipynb
```

atau buka menggunakan Google Colab.

### 4. Siapkan Dataset

Pastikan dataset Aksara Kaganga telah tersedia pada direktori yang sesuai sebelum menjalankan proses pelatihan model.

---

## Output Program

Program menghasilkan:

- Model CNN Terlatih (`model_kaganga.keras`)
- Grafik Accuracy
- Grafik Loss
- Confusion Matrix
- Hasil Prediksi Klasifikasi Aksara Kaganga

---

## Kesimpulan

Berdasarkan implementasi yang dilakukan, metode Convolutional Neural Network (CNN) mampu digunakan untuk melakukan klasifikasi Aksara Kaganga secara otomatis. Model dapat mempelajari pola karakter dari dataset gambar dan menghasilkan prediksi yang baik. Hasil ini menunjukkan bahwa teknologi Deep Learning dapat dimanfaatkan dalam pelestarian dan digitalisasi aksara daerah.
