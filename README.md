# Klasifikasi Suara Instrumen Musik Menggunakan Feature Extraction MFCC, SVM, dan Random Forest

## Deskripsi Proyek
Proyek ini membangun sistem klasifikasi empat instrumen musik (Drum, Gitar, Piano, Violin) dari sinyal audio menggunakan ekstraksi fitur MFCC, delta, dan delta2 MFCC (78 dimensi). Dataset Kaggle (2.629 audio) diproses melalui Random Under-Sampling, MinMaxScaler, lalu diklasifikasikan dengan SVM (RBF) dan Random Forest. SVM unggul dengan akurasi 64,15% (validasi) dan 57,50% (test).

## Tujuan
- Membangun sistem klasifikasi instrumen musik berbasis sinyal audio dengan fitur MFCC.
- Membandingkan performa SVM dan Random Forest dalam klasifikasi audio.
- Menentukan algoritma terbaik berdasarkan accuracy, precision, recall, dan F1-score.

## Tools & Library
- Python
- Librosa (ekstraksi MFCC)
- Scikit-learn (SVM, Random Forest, preprocessing)
- Pandas, NumPy (manipulasi data)
- Matplotlib, Seaborn (visualisasi)
- Google Colab

## Tahapan Proyek
1. **Persiapan Data** - Unduh dataset dari Kaggle (2.629 file audio, 4 kelas)
2. **Ekstraksi Fitur** - MFCC + delta + delta2 (13 koefisien × 6 statistik = 78 dimensi)
3. **EDA** - Distribusi kelas, waveform, spectrogram, heatmap MFCC, boxplot
4. **Preprocessing** - Random Under-Sampling, Label Encoding, MinMaxScaler, split 80:20
5. **Pemodelan** - SVM (RBF, C=10) dan Random Forest (100 estimator)
6. **Evaluasi** - Accuracy, precision, recall, F1-score, confusion matrix

## Hasil
| Model | Accuracy (Val) | F1-Score (Val) | Accuracy (Test) | F1-Score (Test) |
|---|---|---|---|---|
| SVM | 64,15% | 63,97% | 57,50% | 54,03% |
| Random Forest | 58,96% | 58,50% | 47,50% | 42,00% |

- **SVM** unggul pada seluruh metrik evaluasi.
- Kedua model sangat baik pada kelas **Gitar** dan **Piano** (F1-score >0.95).
- Kedua model kesulitan membedakan **Drum** dan **Violin** karena distribusi fitur yang tumpang tindih.

## File Terkait
- Notebook (./notebook/klasifikasi_instrumen.ipynb) - Notebook utama
- 🎵 Dataset: Musical Instruments Sound Dataset v3 (Kaggle)<br>(https://www.kaggle.com/datasets/soumendraprasad/musical-instruments-sound-dataset)

## Author
**Fauziah Roikhana Wardah** (dan tim Kelompok 07)
- Program Studi S1 Sains Data, Universitas Negeri Surabaya
- Email: fauziahroikhana@gmail.com
