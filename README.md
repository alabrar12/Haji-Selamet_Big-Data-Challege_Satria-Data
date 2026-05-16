# MBG Tweet Classification - Hierarchical Ensemble

## Deskripsi
Proyek ini merupakan sistem klasifikasi sentimen tweet menggunakan pendekatan:
- IndoBERT
- XLM-RoBERTa
- Hierarchical Ensemble (Fold → Model)
- Softmax Temperature Weighting
- Threshold Tuning

Metric utama: Balanced Accuracy

---

## Struktur Pipeline

1. Preprocessing:
   - Emoji normalization
   - Slang normalization
   - Text cleaning

2. Data Split:
   - Train → K-Fold (5 fold)
   - Holdout (20%)

3. Training:
   - Model: IndoBERT & XLM-R
   - Loss: CrossEntropy + class weights
   - Early stopping

4. Ensemble:
   - Level 1: Fold ensemble (intra-model)
   - Level 2: Model ensemble (inter-model)

5. Threshold Tuning:
   - Confidence-based fallback class

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

## Output

File hasil prediksi:


---

## Catatan

- Model menggunakan GPU jika tersedia
- Checkpoint model disimpan di folder `models/`
- Dataset diletakkan di folder `data/`

---

## Author
Haji Selamet: [Muhammad Al Abrar, Rafi Ikbar Fahrezy, dan Anjaly Fatimah Mardiyana]
