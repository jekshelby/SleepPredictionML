# Machine Learning Project: Predicting Sleep Quality with Explanatory & Fairness Analysis

## 🎯 Tujuan Proyek

Proyek ini adalah implementasi end-to-end dari sebuah alur kerja Machine Learning yang bertujuan untuk memprediksi kualitas tidur individu. Selain membangun model prediktif, proyek ini juga menekankan pada interpretasi model dan analisis keadilan (fairness) untuk memastikan bahwa prediksi yang dihasilkan adalah akurat dan tidak bias.

## 📊 Dataset

Dataset yang digunakan dalam proyek ini adalah **Sleep Quality Dataset**. Dataset ini berisi berbagai fitur demografi dan gaya hidup yang berpotensi memengaruhi kualitas tidur.

Anda dapat mengunduh dataset ini dari Kaggle:
[Sleep Quality Dataset on Kaggle](https://www.kaggle.com/datasets/hedyma/sleep-quality-dataset)

Pastikan file `Sleep_Quality_Dataset.txt` ditempatkan di direktori yang sama dengan skrip Python Anda.

## 🚀 Metodologi & Alur Kerja

Repositori ini mengikuti alur kerja Machine Learning standar dengan fokus tambahan pada interpretasi dan keadilan:

### 1. Data Preprocessing
Tahap ini melibatkan pembersihan, transformasi, dan rekayasa fitur data tidur. Langkah-langkah utama meliputi:
- Menghapus kolom yang tidak relevan ('User ID').
- Mengubah kolom 'Gender' menjadi format numerik.
- Menghitung 'Sleep Duration' dari 'Bedtime' dan 'Wake-up Time'.
- Melakukan One-Hot Encoding untuk fitur-fitur kategorikal lainnya.

### 2. Exploratory Data Analysis (EDA)
Analisis data eksplorasi dilakukan untuk memahami distribusi data, mengidentifikasi pola, dan menemukan korelasi antar variabel. Ini melibatkan berbagai visualisasi seperti histogram, countplot, heatmap korelasi, dan box plot.

### 3. Pemilihan & Pelatihan Model
Kami mengembangkan dan melatih model regresi untuk memprediksi 'Sleep Quality'. Dua jenis model berbasis pohon dieksplorasi:
- **RandomForestRegressor**: Model ensemble yang dikenal karena akurasi dan robust-nya.
- **DecisionTreeRegressor**: Model tunggal yang lebih sederhana, dengan fokus pada interpretasi dan penyetelan hyperparameter.

### 4. Penyetelan Model (Hyperparameter Tuning)
Untuk mengoptimalkan kinerja `DecisionTreeRegressor`, kami melakukan penyetelan hyperparameter menggunakan `GridSearchCV`. Ini membantu menemukan kombinasi parameter terbaik untuk mengurangi overfitting dan meningkatkan generalisasi model.

### 5. Evaluasi Model
Model dievaluasi secara komprehensif menggunakan metrik standar untuk masalah regresi:
- **Mean Squared Error (MSE)**: Mengukur rata-rata kuadrat kesalahan prediksi.
- **R2 Score (Coefficient of Determination)**: Menunjukkan proporsi varians dalam variabel target yang dapat dijelaskan oleh model.
Evaluasi dilakukan pada data validasi dan data uji untuk mendapatkan gambaran kinerja yang objektif.

### 6. Analisis Fitur Terpenting (Feature Importance)
Setelah pelatihan model, kami mengidentifikasi fitur-fitur yang paling berpengaruh terhadap prediksi kualitas tidur. Visualisasi bar plot digunakan untuk menampilkan prioritas fitur-fitur ini.

### 7. Analisis Keadilan Model (Fairness Metrics)
Aspek krusial dari proyek ini adalah analisis keadilan model. Menggunakan pustaka `fairlearn`, kami memeriksa potensi bias kinerja model terhadap kelompok demografi yang berbeda (khususnya gender) untuk memastikan prediksi yang adil dan tidak diskriminatif.

## 🛠️ Teknologi & Pustaka

Proyek ini dikembangkan menggunakan Python dan memanfaatkan pustaka-pustaka berikut:
-   `pandas`
-   `numpy`
-   `matplotlib`
-   `seaborn`
-   `scikit-learn`
-   `fairlearn`

## 🚀 Cara Menjalankan Kode

1.  **Kloning repositori ini:**
    ```bash
    git clone [https://github.com/jekshelby/SleepPredictionML.git]
    ```
2.  **Instal dependensi yang diperlukan:**
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn fairlearn
    ```
3.  **Pastikan dataset ada:** Unduh `Sleep_Quality_Dataset.txt` dari tautan Kaggle di atas dan tempatkan di direktori yang sama dengan skrip Python.
4.  **Jalankan skrip Python:**
    ```bash
    SleepPrediciton.ipynb
    ```
    
## ✍️ Kontributor

- [Muhammad Dzaky Ahnaf](https://github.com/jekshelby).

---