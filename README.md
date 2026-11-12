# 🇮🇩 Indonesian Government Hoax News Dataset

Kumpulan dataset berita hoaks bertema pemerintahan Indonesia yang telah disiapkan dan dibersihkan, siap digunakan untuk keperluan penelitian, pengembangan model *Machine Learning*, pemrosesan bahasa alami (*Natural Language Processing* / NLP), serta pembuatan sistem deteksi berita palsu (*Fake News Detection*).

---

## 📂 Struktur Dataset

Repository ini terdiri dari beberapa file utama:

1. **`Data_latih.csv`** (Training Set)
   * Berisi data teks berita (hoaks maupun fakta) yang digunakan untuk melatih model *Machine Learning* atau *Deep Learning*.
2. **`Data_uji.csv`** (Testing Set)
   * Berisi data uji independen yang digunakan untuk mengevaluasi performa dan akurasi model yang telah dilatih.
3. **`dataset_news.csv`**
   * Gabungan atau kumpulan data mentah/tambahan berita seputar isu pemerintahan.

---

## 📊 Deskripsi Kolom Data

Setiap file CSV umumnya memiliki struktur kolom sebagai berikut:
* **`text` / `content`**: Isi atau narasi berita yang dianalisis.
* **`label` / `category`**: Label kelas data (Contoh: `0` untuk Berita Valid/Fakta dan `1` untuk Berita Hoaks, atau *string* kategorikal lainnya).

---

## 🚀 Cara Cepat Memuat Dataset (Python & Pandas)

Anda dapat dengan mudah memuat dataset ini ke dalam project Python menggunakan pustaka `pandas`:

```python
import pandas as pd

# Memuat data latih (training set)
df_train = pd.read_csv('Data_latih.csv')
print("Jumlah data latih:", df_train.shape)
print(df_train.head())

# Memuat data uji (testing set)
df_test = pd.read_csv('Data_uji.csv')
print("Jumlah data uji:", df_test.shape)
