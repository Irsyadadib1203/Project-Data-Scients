# 📘 Judul Proyek
*(Isi judul proyek Anda di sini)*

## 👤 Informasi
- **Nama:** [Irsyad Adib Ahsani]  
- **Repo:** [https://github.com/Irsyadadib1203/Project-Data-Scients.git]  
- **Video:** [https://drive.google.com/drive/folders/15FPwEJvxV_e4yD8GXT_sGBTETr6KDohZ?usp=sharing]  

---

# 1. 🎯 Ringkasan Proyek
Proyek ini membandingkan tiga pendekatan pemodelan—Baseline (Logistic Regression), Advanced Machine Learning (Random Forest), dan Deep Learning (Multilayer Perceptron / MLP)—untuk melakukan prediksi risiko kredit (credit risk classification) menggunakan German Credit Dataset.

Tujuan utama dari proyek ini adalah menentukan model terbaik dalam mengklasifikasikan risiko kredit serta memahami faktor-faktor finansial dan demografis yang paling berpengaruh terhadap kelayakan kredit nasabah.

✅ Pencapaian Utama

- Melakukan Exploratory Data Analysis (EDA) untuk memahami distribusi data dan karakteristik nasabah
- Membangun pipeline data preprocessing yang terstruktur dan reproducible
- Mengembangkan dan melatih tiga model klasifikasi dengan kompleksitas berbeda
- Mengevaluasi performa model menggunakan metrik klasifikasi (Accuracy, Confusion Matrix,   
  Classification Report)
- Membandingkan performa Baseline vs Advanced ML vs Deep Learning
- Mengidentifikasi model terbaik berdasarkan akurasi dan stabilitas performa
- Menyimpan model dan preprocessing untuk reuse dan deployment

# 2. 📄 Problem & Goals
**Problem Statements:**  
- Dataset kredit memiliki pola hubungan non-linear antara fitur finansial (durasi kredit, jumlah 
  pinjaman, status pekerjaan, riwayat kredit) dan risiko gagal bayar
- Model linear sederhana memiliki keterbatasan dalam menangkap interaksi kompleks antar fitur
- Diperlukan sistem prediksi risiko kredit yang akurat dan konsisten untuk mendukung pengambilan  
  keputusan finansial 

**Goals:**  
- Membangun dan membandingkan tiga pendekatan model klasifikasi:
    1. Baseline: Logistic Regression
    2. Advanced ML: Random Forest (Tuned)
    3. Deep Learning: Multilayer Perceptron (MLP)
- Mengevaluasi performa model menggunakan metrik:
    1. Accuracy
    2. Confusion Matrix
    3. Precision, Recall, dan F1-score
- Menentukan model terbaik untuk prediksi risiko kredit
- Menghasilkan pipeline analisis yang modular, rapi, dan reproducible 

---
## 📁 Struktur Folder
```
project/
│
├── data/                   # Dataset (tidak di-commit, download manual)
│
├── notebooks/              # Jupyter notebooks
│   └── ML_Project.ipynb
│
├── src/                    # Source code
│   
├── models/                 # Saved models
│   ├── model_baseline.pkl
│   ├── model_rf.pkl
│   └── model_cnn.h5
│
├── images/                 # Visualizations
│   └── r
│
├── requirements.txt        # Dependencies
├── .gitignore
└── README.md
```
---

# 3. 📊 Dataset
- **Sumber:** UCI Machine Learning Repository (Statlog – German Credit Data)
- **Jumlah Data:** 1.000 data pemohon kredit
- **Jumlah Fitur:** 20 fitur (campuran numerik dan kategorikal)
- **Tipe:** Data tabular untuk tugas klasifikasi biner
- **Target:** Status risiko kredit (Good Credit / Bad Credit)


### Fitur Utama
| Fitur | Deskripsi |
|------|-----------|
| Status_Akun | Status rekening giro pemohon |
| Durasi_Kredit | Lama durasi kredit (bulan) |
| Riwayat_Kredit | Riwayat kredit sebelumnya |
| Tujuan_Kredit | Tujuan pengajuan kredit |
| Jumlah_Kredit | Jumlah kredit yang diajukan |
| Tabungan | Status tabungan pemohon |
| Lama_Bekerja | Lama bekerja di pekerjaan saat ini |
| Rasio_Cicilan | Persentase cicilan terhadap pendapatan |
| Status_Perkawinan | Status perkawinan dan jenis kelamin |
| Penjamin | Keberadaan penjamin |
| Lama_Tinggal | Lama tinggal di alamat saat ini |
| Aset | Kepemilikan aset |
| Umur | Umur pemohon |
| Kredit_Lain | Kepemilikan kredit lain |
| Status_Rumah | Status kepemilikan rumah |
| Jumlah_Kredit_Berjalan | Jumlah kredit yang sedang berjalan |
| Pekerjaan | Jenis pekerjaan |
| Jumlah_Tanggungan | Jumlah tanggungan |
| Telepon | Kepemilikan telepon |
| Pekerja_Asing | Status pekerja asing |
| Target | Risiko kredit (Good / Bad) |


---

# 4. 🔧 Data Preparation
1. Data Cleaning
    ✅ Tidak ada missing values
    ✅ Tidak ada data duplikat
    ✅ Outliers dipertahankan (valid secara klinis)
2. Data Transformation
    Standardization: StandardScaler untuk normalisasi fitur (mean=0, std=1)
3. Data Splitting
    Training: 800 samples (80%)
    Testing: 200 samples (20%)

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:** Logistic Regression  
  Digunakan sebagai model baseline karena sederhana, cepat dilatih, dan mudah diinterpretasikan. Logistic Regression berfungsi sebagai pembanding awal untuk mengevaluasi peningkatan performa dari model yang lebih kompleks dalam memprediksi risiko kredit (Good/Bad Credit).

- **Model 2 – Advanced ML:** Random Forest Classifier  
  Digunakan untuk menangkap hubungan non-linear dan interaksi kompleks antar fitur finansial dan demografis. Random Forest juga memberikan kestabilan performa serta kemampuan mengurangi overfitting melalui mekanisme ensemble.

- **Model 3 – Deep Learning:** Multilayer Perceptron (MLP)  
  Digunakan untuk mempelajari pola non-linear tingkat tinggi pada data tabular. Model ini terdiri dari beberapa hidden layer dengan fungsi aktivasi ReLU dan regularisasi Dropout untuk meningkatkan generalisasi.


---

# 6. 🧪 Evaluation
| Model | Accuracy | F1-Score |
|------|----------|----------|
| Logistic Regression (Baseline) | 0.780 | 0.85 |
| Random Forest (Tuned) | 0.760 | 0.84 |
| Deep Learning (MLP) | 0.745 | 0.83 |


### Hasil Singkat
| Model | Score | Catatan |
|-------|-------|---------|
| Baseline (Logistic Regression) | 0.780 | Model sederhana, cepat dilatih, dan mudah diinterpretasikan sebagai pembanding awal |
| Advanced (Random Forest) | 0.760 | Mampu menangkap hubungan non-linear dan interaksi fitur dengan performa stabil |
| Deep Learning (MLP) | 0.745 | Menangkap pola kompleks pada data tabular, namun memerlukan tuning dan regularisasi |

---

# 7. 🏁 Kesimpulan
- **Model terbaik:** Logistic Regression (Baseline)

- **Alasan:**  
  Berdasarkan hasil evaluasi, Logistic Regression memperoleh nilai akurasi tertinggi (78%) dibandingkan Random Forest (76%) dan Deep Learning MLP (74.5%). Meskipun merupakan model paling sederhana, Logistic Regression mampu melakukan generalisasi dengan baik pada dataset Statlog (German Credit Data) yang berukuran relatif kecil dan bersifat tabular. Selain itu, waktu pelatihan Logistic Regression masih berada pada tingkat yang wajar.

- **Insight penting:**  
  1. Dataset German Credit memiliki pola yang relatif dapat dipisahkan secara linear, sehingga model linear seperti Logistic Regression dapat bekerja sangat efektif.  
  2. Model yang lebih kompleks seperti Random Forest dan MLP tidak selalu memberikan performa lebih baik pada dataset tabular berukuran kecil hingga menengah.  
  3. Deep Learning (MLP) membutuhkan waktu pelatihan paling lama, namun tidak menghasilkan peningkatan akurasi yang signifikan dibandingkan model lainnya.  
  4. Pemilihan model terbaik harus mempertimbangkan keseimbangan antara akurasi, kompleksitas model, dan efisiensi komputasi, bukan hanya kompleksitas arsitektur.


---

# 8. 🔮 Future Work
- [ ] **Tambah data**  
  Menggunakan dataset risiko kredit tambahan atau data historis dengan jumlah sampel lebih besar untuk meningkatkan kemampuan generalisasi model, terutama pada kelas *Bad Credit* yang jumlahnya lebih sedikit.

- [ ] **Tuning model**  
  Melakukan hyperparameter tuning lebih lanjut pada Random Forest (jumlah tree, depth, dan split criteria) serta Logistic Regression (regularisasi dan solver) untuk meningkatkan performa model.

- [ ] **Coba arsitektur Deep Learning lain**  
  Mengeksplorasi arsitektur deep learning alternatif untuk data tabular seperti:
  - MLP dengan batch normalization
  - TabNet atau Wide & Deep Network
  - Neural Network dengan embedding untuk fitur kategorikal

- [ ] **Deployment**  
  Mengimplementasikan model terbaik ke dalam aplikasi sederhana (REST API atau web app) untuk simulasi sistem penilaian risiko kredit secara real-time.


---

# 9. 🔁 Reproducibility
Gunakan environment:
