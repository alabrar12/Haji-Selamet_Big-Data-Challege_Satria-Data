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
