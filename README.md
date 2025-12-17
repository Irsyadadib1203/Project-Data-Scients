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
- **Sumber:** [...]  
- **Jumlah Data:** [...]  
- **Tipe:** [...]  

### Fitur Utama
| Fitur | Deskripsi |
|------|-----------|
| ... | ... |

---

# 4. 🔧 Data Preparation
- Cleaning (missing/duplicate/outliers)  
- Transformasi (encoding/scaling)  
- Splitting (train/val/test)  

---

# 5. 🤖 Modeling
- **Model 1 – Baseline:** [...]  
- **Model 2 – Advanced ML:** [...]  
- **Model 3 – Deep Learning:** [...]  

---

# 6. 🧪 Evaluation
**Metrik:** Accuracy / F1 / MAE / MSE (pilih sesuai tugas)

### Hasil Singkat
| Model | Score | Catatan |
|-------|--------|---------|
| Baseline | [...] | |
| Advanced | [...] | |
| Deep Learning | [...] | |

---

# 7. 🏁 Kesimpulan
- Model terbaik: [...]  
- Alasan: [...]  
- Insight penting: [...]  

---

# 8. 🔮 Future Work
- [ ] Tambah data  
- [ ] Tuning model  
- [ ] Coba arsitektur DL lain  
- [ ] Deployment  

---

# 9. 🔁 Reproducibility
Gunakan environment:
