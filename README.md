# Kelompok_5_Tugas02_Linear_Regression

# Prediksi Biaya Medis (Medical Cost Prediction)

## Ikhtisar
Proyek ini bertujuan untuk memprediksi biaya medis berdasarkan faktor-faktor individu seperti usia, BMI, jumlah anak, riwayat merokok, jenis kelamin, dan wilayah. Dengan menggunakan teknik machine learning, kami mengembangkan model regresi untuk memperkirakan biaya perawatan kesehatan secara akurat.

## Informasi Proyek
- **Mata Kuliah:** Machine Learning
- **Dosen Pengampu:** Alim Misbullah, S.Si., M.S.
- **Kelompok:** 5
- **Anggota Kelompok:**
  - Mila Lestari (2208107010002)
  - Zahra Zafira (2208107010040)
  - Pryta Rosela (2208107010046)
  - Cut Sula Fhatia Rahma (2208107010048)
  - Widya Nurul Sukma (2208107010054)

## Dataset
Dataset Prediksi Biaya Medis berisi informasi tentang pasien dan biaya medis mereka, digunakan untuk memprediksi biaya pengobatan berdasarkan faktor-faktor individu.

**Dataset:** [Medical Insurance Cost Prediction](https://www.kaggle.com/datasets/rahulvyasm/medical-insurance-cost-prediction)

**Fitur:**
- Usia (Age)
- Indeks Massa Tubuh (BMI)
- Jumlah Anak (Children)
- Riwayat Merokok (Smoker)
- Jenis Kelamin (Sex)
- Wilayah (Region)

**Variabel Target:**
- Biaya Medis (charges)

## Metodologi

### Analisis Data
1. **Exploratory Data Analysis (EDA):** Analisis distribusi, penilaian korelasi, dan visualisasi hubungan antar variabel
2. **Feature Engineering:** Label encoding untuk variabel kategori
3. **Pra-pemrosesan Data:** Standardisasi fitur numerik dan pembagian data

### Model yang Diimplementasikan
1. **Regresi Linear:** Pendekatan dasar untuk membentuk baseline
2. **Regresi Polinomial (derajat=2):** Untuk menangkap hubungan yang lebih kompleks antar fitur

### Metrik Evaluasi
- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)

## Temuan Utama

### Analisis Korelasi
- Korelasi positif kuat antara status merokok dan biaya medis
- Korelasi positif sedang antara usia dan biaya medis
- Korelasi positif sedang antara BMI dan biaya medis

### Wawasan Demografis
- Perokok memiliki biaya medis yang jauh lebih tinggi dibandingkan non-perokok
- Wilayah Southeast menunjukkan biaya yang lebih tinggi dibandingkan wilayah lain
- Laki-laki memiliki kecenderungan sedikit lebih tinggi untuk merokok dibandingkan perempuan

### Performa Model
| Model | MAE | MSE | RMSE |
|-------|-----|-----|------|
| Regresi Linear | 0,1231 | 0,0377 | 0,1942 |
| Regresi Polinomial | 0,0872 | 0,0269 | 0,1640 |

Regresi Polinomial (derajat 2) mengungguli Regresi Linear dalam semua metrik evaluasi, yang menunjukkan bahwa hubungan antara fitur dan biaya medis tidak sepenuhnya linear.

## Cara Penggunaan

### Prasyarat
- Python 3.x
- Library yang diperlukan: numpy, pandas, matplotlib, seaborn, scikit-learn

### Instalasi
```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

### Eksekusi
1. Clone repositori
2. Tempatkan dataset `insurance.csv` di direktori proyek
3. Jalankan notebook Jupyter atau skrip Python

## Visualisasi
Proyek ini mencakup berbagai visualisasi:
- Plot distribusi untuk biaya, BMI, dan usia
- Heatmap korelasi antar variabel
- Barplot untuk distribusi biaya berdasarkan wilayah
- Countplot untuk analisis demografis
- Boxplot membandingkan biaya di berbagai demografis
- Scatterplot menunjukkan hubungan antara BMI dan biaya
- Perbandingan antara nilai aktual dan nilai prediksi untuk kedua model

## Kesimpulan
Asuransi merupakan kebijakan finansial yang bertujuan untuk mengurangi biaya yang ditimbulkan akibat kecelakaan atau penyakit. Biaya ini dapat dipengaruhi oleh berbagai faktor seperti usia, BMI, jumlah anak, status merokok, dan wilayah tempat tinggal.

Melalui proyek ini, kami menggunakan teknik regresi untuk memprediksi biaya asuransi berdasarkan fitur-fitur tersebut, serta membandingkan performa model berdasarkan metrik evaluasi.

Regresi Polinomial memberikan performa yang lebih baik dibandingkan Regresi Linear, ditunjukkan dengan nilai error yang lebih kecil pada semua metrik (MAE, MSE, dan RMSE). Ini mengindikasikan bahwa hubungan antara fitur dan biaya medis tidak sepenuhnya linear, dan model polinomial dapat menangkap kompleksitas hubungan tersebut dengan lebih baik.
