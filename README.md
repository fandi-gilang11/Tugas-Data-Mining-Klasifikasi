# Proyek Data Mining: Klasifikasi Aktivitas Manusia

Repository ini berisi tugas mata kuliah Data Mining yang diadaptasi dari materi Coursera "Supervised Machine Learning: Classification". Proyek ini berfokus pada penerapan model Regresi Logistik untuk mengklasifikasikan aktivitas manusia berdasarkan data sensor *smartphone*.

## Deskripsi Dataset
Dataset yang digunakan merupakan modifikasi dari *Human Activity Recognition (HAR) database*. Modifikasi yang dilakukan untuk memenuhi spesifikasi tugas meliputi:
1. Translasi label kelas target ke dalam Bahasa Indonesia (contoh: Berjalan, Duduk, Berdiri).
2. Penambahan *noise* variasi acak (distribusi normal) pada nilai numerik fitur untuk memastikan data unik, namun tetap menjaga pola agar tidak merusak performa klasifikasi mesin.
3. *Resampling* dan reduksi jumlah baris (menjadi ~20% dari ukuran asli) guna mengoptimalkan ukuran file agar kompatibel dengan limitasi unggahan GitHub web (<25 MB).

## Metodologi
Alur kerja yang diterapkan dalam *notebook* ini mengacu pada teknik yang dipelajari:
* **Preprocessing:** Penyesuaian label menggunakan `LabelEncoder`.
* **Data Splitting:** Menggunakan `StratifiedShuffleSplit` (70% Train, 30% Test) untuk menjaga keseimbangan proporsi setiap kelas aktivitas.
* **Modeling:** Menggunakan `LogisticRegression` dengan solver `liblinear` dan pendekatan One-vs-Rest (OVR).
* **Evaluasi:** Menggunakan metrik *Accuracy*, *Precision*, *Recall*, *F1-Score*, dan divisualisasikan menggunakan *Confusion Matrix Heatmap*.

## Struktur File
* `HAR_Modified_Final.csv`: Dataset yang telah dimodifikasi.
* `Model_Klasifikasi_Aktivitas.ipynb`: *Jupyter Notebook* berisi seluruh kode pra-pemrosesan, pelatihan model, dan evaluasi.

## Hasil Singkat
Model Regresi Logistik mampu mengenali pola aktivitas manusia dengan tingkat akurasi yang sangat baik. Detail *Confusion Matrix* dapat dilihat pada hasil eksekusi *notebook*.
