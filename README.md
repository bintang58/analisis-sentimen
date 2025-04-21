# 📦 Submission - Analisis Sentimen

Repositori ini berisi proyek akhir dari modul **Analisis Sentimen** dalam pelatihan **Laskar AI - Belajar Pengembangan Machine Learning**. Proyek ini mencakup dua tahap:

1. 🧾 **Scraping** – Mengambil data ulasan aplikasi dari Google Play Store menggunakan `google-play-scraper`.
2. 🧠 **Analisis Sentimen** – Melatih model klasifikasi sentimen dari teks ke dalam tiga kategori: **negatif**, **netral**, dan **positif**.

---

## 📁 Struktur Folder

| Nama File | Deskripsi |
|-----------|-----------|
| `[Scraping]_Submission_Pertama_BPML_Bintang_Cahya_Anwar.ipynb` | Notebook scraping data ulasan aplikasi |
| `[Analisis_Sentimen]_Submission_Pertama_BPML_Bintang_Cahya_Anwar.ipynb` | Notebook eksplorasi, preprocessing, dan pelatihan model |
| `dataset_scraping.csv` | Dataset hasil scraping dari Google Play |
| `requirements.txt` | Daftar pustaka yang digunakan |
| `README.md` | Dokumentasi proyek ini |

---

## 📂 Dataset

Dataset diperoleh dengan scraping aplikasi dari Google Play Store menggunakan `google-play-scraper`. Dataset terdiri dari ribuan ulasan aplikasi dalam Bahasa Indonesia.

---

## 🛠️ Teknologi yang Digunakan

### 📚 Bahasa & Pustaka

- **Python**:
  - `os`, `re`, `string`, `csv`, `requests`, `datetime`, `io` – Utilitas dasar dan manajemen file
  - `numpy`, `pandas` – Manipulasi dan analisis data

### 📊 Visualisasi:
  - `matplotlib.pyplot`, `seaborn` – Visualisasi grafik dan distribusi data
  - `wordcloud.WordCloud` – Membuat visualisasi Word Cloud

### 🔤 Natural Language Processing (NLP):
  - `nltk` – Tokenisasi dan stopword removal
    - `word_tokenize`, `stopwords`
    - `nltk.download('punkt')`, `stopwords`, dll.
  - `Sastrawi` – Library Bahasa Indonesia untuk:
    - `StemmerFactory` – Stemming kata
    - `StopWordRemoverFactory` – Menghapus kata berhenti

### 🧠 Machine Learning:
  - `TfidfVectorizer` – Ekstraksi fitur teks
  - `LabelEncoder` – Encoding label kategorikal
  - `train_test_split` – Membagi dataset untuk pelatihan dan pengujian
  - `sklearn.metrics` – Evaluasi model:
    - `accuracy_score`, `precision_score`, `recall_score`, `f1_score`, `classification_report`

### 🤖 Deep Learning (TensorFlow / Keras):
  - `Tokenizer`, `pad_sequences` – Tokenisasi teks dan padding
  - `Sequential` – Arsitektur model
  - `Dense`, `Dropout`, `LSTM`, `GRU`, `Conv1D`, `MaxPooling1D`, `Flatten` – Layer jaringan
  - `Adam` – Optimizer
  - `EarlyStopping` – Callback untuk menghentikan pelatihan lebih awal
  - `l2` – Regularisasi

### 🌐 Web Scraping:
  - `google-play-scraper` – Scraping ulasan dari Google Play Store
    - `reviews_all` – Mengambil seluruh review aplikasi
    - `Sort` – Mengatur urutan review

### ☁️ Google Colab:
  - `google.colab.drive` – Mengakses file dari Google Drive

### 🔧 Konfigurasi:
  - `pd.options.mode.chained_assignment = None` – Menonaktifkan warning chaining assignment di Pandas
  - `np.random.seed(0)` – Menetapkan seed untuk hasil yang reprodusibel

---

## 🚀 Menjalankan Proyek

### 1. Jalankan di Google Colab

> Cocok untuk pengguna yang tidak ingin setup environment lokal.

1. Buka [Google Colab](https://colab.research.google.com).
2. Klik **File > Open notebook > GitHub**.
3. Masukkan URL repositori ini.
4. Pilih file notebook yang ingin dijalankan:
   - `[Scraping]_Submission_Pertama_BPML_Bintang_Cahya_Anwar.ipynb`
   - `[Analisis_Sentimen]_Submission_Pertama_BPML_Bintang_Cahya_Anwar.ipynb`
5. Upload file `dataset_scraping.csv` melalui sidebar **Files → Upload**.

### 2. Jalankan Secara Lokal

1. Clone repository ini:
   ```bash
   git clone https://github.com/bintang58/analisis-sentimen
   cd analisis-sentimen
2. Buat dan aktifkan environment (opsional, tapi disarankan):
   ```bash
   python -m venv nama_venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
3. Install dependensi:
   ```bash
   pip install -r requirements.txt
4. Jalankan notebook menggunakan Jupyter atau Jupyter Lab:
   ```bash
   jupyter notebook

---

## 📝 Catatan

- Dataset scraping tidak otomatis tersedia karena berasal dari scraping live dari Google Play. Namun, file `dataset_scraping.csv` telah disertakan.
- Notebook scraping hanya perlu dijalankan ulang jika ingin mengumpulkan data terbaru.
- Proyek ini menggunakan berbagai teknik machine learning dan deep learning untuk klasifikasi sentimen teks, dengan tujuan mencapai akurasi minimal 85% (disarankan di atas 92%).

---

> Proyek ini diibuat sebagai bagian dari pelatihan **Laskar AI - Belajar Pengembangan Machine Learning**
