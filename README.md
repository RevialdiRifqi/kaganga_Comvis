# Klasifikasi Aksara Kaganga Menggunakan Convolutional Neural Network (CNN)

Tugas Kelompok

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

Proyek ini merupakan implementasi metode **Convolutional Neural Network (CNN)** untuk melakukan klasifikasi citra **Aksara Kaganga**. Model dikembangkan menggunakan Python dan TensorFlow untuk mengenali karakter aksara secara otomatis berdasarkan dataset citra yang telah diproses.

## Tujuan

- Memahami konsep Deep Learning dan CNN.
- Menerapkan CNN pada klasifikasi citra.
- Melatih dan mengevaluasi model klasifikasi Aksara Kaganga.
- Menganalisis performa model menggunakan metrik evaluasi.

## Teknologi yang Digunakan

- Python
- TensorFlow
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- Google Colab

## Struktur Repository

```text
.
├── Untitled1.ipynb
├── model_kaganga.keras
├── dataset/
└── README.md
```

## Metode

### Data Augmentation

- Rescale = 1/255
- Rotation Range = 10°
- Zoom Range = 0.1
- Width Shift Range = 0.1
- Height Shift Range = 0.1

### Arsitektur CNN

1. Input Layer (64×64×3)
2. Convolution Layer (32 Filter)
3. Max Pooling Layer
4. Convolution Layer (64 Filter)
5. Max Pooling Layer
6. Convolution Layer (128 Filter)
7. Max Pooling Layer
8. Flatten Layer
9. Dense Layer
10. Output Layer (Softmax)

### Parameter Pelatihan

- Epoch : 15
- Batch Size : 32
- Optimizer : Adam
- Loss Function : Categorical Crossentropy

## Hasil

Model dievaluasi menggunakan:

- Accuracy Curve
- Loss Curve
- Confusion Matrix
- Akurasi Prediksi

## Cara Menjalankan

### Install Dependency

```bash
pip install tensorflow numpy matplotlib seaborn scikit-learn
```

### Jalankan Notebook

```bash
jupyter notebook Untitled1.ipynb
```

atau buka menggunakan Google Colab.

## Kesimpulan

Model CNN yang dibangun mampu melakukan klasifikasi Aksara Kaganga dengan baik melalui proses pelatihan dan pengujian. Hasil yang diperoleh menunjukkan bahwa metode Deep Learning dapat digunakan sebagai solusi untuk pengenalan aksara daerah secara otomatis.
