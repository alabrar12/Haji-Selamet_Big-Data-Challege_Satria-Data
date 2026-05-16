# MBG Tweet Classification - Multi-Model Ensemble

## Deskripsi
Proyek ini merupakan solusi klasifikasi sentimen tweet menggunakan pendekatan deep learning berbasis transformer dengan teknik ensemble multi-model.

Model yang digunakan:
- IndoBERT
- XLM-RoBERTa

Metode:
- Holdout split (20%)
- 5-Fold Cross Validation
- Ensemble logits (fold-level + model-level)
- Threshold tuning (confidence-based)

Metric evaluasi:
- Balanced Accuracy (BA)

---

## Struktur Proyek

---

## Cara Menjalankan

### 1. Install dependencies

### 1.1 Library
- torch
- transformers
- scikit-learn
- pandas
- numpy
- scipy

### 1.2 ubah path DATA_DIR, sesuai dengan dataset disimpan.

### 2. Jalankan program


---

## Alur Program

1. Load dataset (train & test)
2. Preprocessing teks:
   - lowercasing
   - hapus URL
   - normalisasi mention & hashtag
3. Encoding label
4. Split data:
   - 80% untuk training (K-Fold)
   - 20% holdout (evaluasi final)
5. Training model:
   - 5-Fold CV per model
   - Early stopping
6. Ensemble:
   - Level 1: antar fold
   - Level 2: antar model
7. Threshold tuning:
   - meningkatkan Balanced Accuracy
8. Inference pada test set
9. Generate file submission

---

## Output

File hasil prediksi:

---

## Kebutuhan Sistem

- Python >= 3.8
- GPU (disarankan)
- RAM minimal 8GB

---

## Catatan

- Seed digunakan: 42 (reproducible)
- Ensemble menggunakan logits (bukan voting)
- Model dapat diperluas dengan menambahkan konfigurasi di `MODEL_CONFIGS`

---

## Author
Haji Selamet: [Muhammad Al Abrar, Rafi Ikbar Fahrezy, dan Anjaly Fatimah Mardiyana]
