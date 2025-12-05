# UTS Machine Learning 

## Purpose of this repository

Repository ini berisi pengerjaan tugas UTS mata kuliah Machine Learning. Fokusnya adalah membangun pipeline end to end untuk tiga jenis masalah: klasifikasi fraud, regresi, dan clustering. Semua eksperimen dikerjakan menggunakan Python dan dijalankan di Google Colab.

## Project overview

a. Fraud detection

Tujuan: memprediksi probabilitas suatu transaksi online bersifat fraud (isFraud) menggunakan dataset train_transaction.csv dan test_transaction.csv.

Isi utama:

* Data preprocessing: pengecekan distribusi target, penanganan missing value dengan SimpleImputer (median), scaling fitur numerik, dan feature engineering sederhana TransactionAmt_log.
* Penanganan class imbalance: penggunaan class_weight="balanced" pada Logistic Regression dan RandomForest.
* Model: Logistic Regression dan RandomForest dengan beberapa kombinasi hyperparameter.
* Evaluasi: Accuracy, Precision, Recall, F1-score, ROC AUC, dan confusion matrix.
* Output: file submission berisi pasangan TransactionID dan probabilitas isFraud untuk data test_transaction.

b. Regression 

Tujuan: memprediksi tahun rilis lagu berdasarkan fitur numerik audio pada file midterm-regresi-dataset.csv.

Isi utama:

* Data preprocessing: pemisahan target dan fitur, penanganan missing value dengan SimpleImputer (median), dan scaling fitur numerik dengan StandardScaler.
* Model: Linear Regression sebagai baseline dan RandomForestRegressor sebagai model non linear.
* Hyperparameter tuning: GridSearchCV sederhana untuk kombinasi n_estimators dan max_depth.
* Evaluasi: MSE, RMSE, MAE, dan R² pada data test, serta interpretasi singkat seberapa baik model mengenali pola tahun rilis.

c. Clustering 

Tujuan: mengelompokkan nasabah kartu kredit berdasarkan perilaku penggunaan kartu pada dataset clusteringmidterm.csv.

Isi utama:

* Data preprocessing: menghapus CUST_ID, menangani missing value dengan SimpleImputer (median), dan scaling fitur numerik dengan RobustScaler untuk mengurangi pengaruh outlier.
* Model: KMeans dengan beberapa nilai k.
* Pemilihan jumlah cluster: perbandingan inertia (elbow method) dan silhouette score untuk memilih k terbaik.
* Evaluasi dan interpretasi: ukuran tiap cluster, rata rata fitur penting per cluster (BALANCE, PURCHASES, CASH_ADVANCE, CREDIT_LIMIT, PAYMENTS, dll), visualisasi hasil cluster dengan PCA 2D, dan penjelasan makna setiap cluster (pengguna ringan vs pengguna aktif).

## How to run the notebooks

1) Buka notebook langsung di Google Colab (Open in Colab atau upload ke Colab).
2) Pastikan file CSV sudah ada di Google Drive atau mengikuti link Colab yang disediakan.
3) Sesuaikan variabel base_path atau path dataset di bagian awal notebook dengan lokasi file di Google Drive kamu.
4) Jalankan cell dari atas ke bawah.

## Files and structure

* Fraud_ML.ipynb  → pipeline deteksi fraud end to end
* Regresi_ML.ipynb      → pipeline regresi prediksi tahun rilis lagu
* Clustering_ML.ipynb      → pipeline clustering nasabah kartu kredit
* README.md                        → penjelasan umum repository ini

## Student information

Name  : Lu'luah Buhairah

Class : TK-46-03

NIM   : 1103220134
