
# 🎬 LayarKita: Sistem Rekomendasi Film Interaktif berbasis Streamlit

**LayarKita** adalah aplikasi rekomendasi film berbasis web yang dibangun menggunakan framework **Streamlit**. Aplikasi ini memanfaatkan pendekatan **Content-Based Filtering** untuk memberikan rekomendasi film yang relevan dengan preferensi pengguna berdasarkan **judul film yang disukai**, **sinopsis**, **genre**, dan **aktor**.

Aplikasi ini juga dilengkapi dengan **fuzzy string matching** untuk mengatasi kesalahan penulisan pada input judul film, serta menyediakan berbagai **visualisasi data interaktif** untuk memperkaya pengalaman pengguna.

---

## 📌 Deskripsi Proyek

Tujuan utama dari proyek ini adalah memberikan solusi bagi pengguna yang ingin menemukan film yang sesuai dengan selera mereka, dengan pendekatan yang personal dan efisien.

### Fitur Utama

- ✅ Pengguna dapat memasukkan **judul film favorit**
- ✅ Menyaring hasil rekomendasi berdasarkan:
  - Tahun rilis
  - Rating film
  - Genre
  - Aktor
- ✅ Sistem dapat mengenali **judul film yang keliru penulisannya (typo)** menggunakan **fuzzy matching**
- ✅ Visualisasi data meliputi:
  - Film dengan **rating tertinggi**
  - Film **terbaru**
  - **Distribusi genre** film

---

## 🧠 Teknologi & Metodologi

- **Bahasa Pemrograman:** Python  
- **Framework Frontend:** Streamlit  
- **Machine Learning:**  
  - TF-IDF Vectorizer untuk representasi teks (overview, genre, aktor)  
  - Cosine Similarity untuk mengukur kemiripan antar film  
  - FuzzyWuzzy (rapidfuzz) untuk pencocokan judul  
- **Visualisasi Data:** Matplotlib & Seaborn

---

## 🗂️ Struktur Dataset

Dataset `Film_300.csv` berisi informasi dari 300 film, dengan kolom sebagai berikut:

| Kolom         | Deskripsi                          |
|---------------|------------------------------------|
| `title`       | Judul film                         |
| `overview`    | Ringkasan/sinopsis film            |
| `name_genres` | Genre film (dipisahkan koma)       |
| `actor_name`  | Aktor utama dalam film             |
| `vote_average`| Rating film                        |
| `release_date`| Tanggal rilis film                 |

> Pastikan semua kolom tersedia dan telah dibersihkan dari missing value sebelum menjalankan aplikasi.

---

## 🛠️ Instalasi

1. **Clone repository ini:**
```bash
git clone https://github.com/username/LayarKita.git
cd LayarKita
```

2. **Install dependencies:**
```bash
pip install -r requirements.txt
```

Jika tidak tersedia file `requirements.txt`, install secara manual:
```bash
pip install pandas streamlit matplotlib seaborn scikit-learn rapidfuzz
```

---

## ▶️ Cara Menjalankan Aplikasi

1. Pastikan file dataset `Film_300.csv` berada dalam direktori yang sama dengan `app.py`.  
   Jika terdapat path lokal di dalam kode, ubah sesuai direktori lokal Anda.

2. Jalankan aplikasi menggunakan perintah:
```bash
streamlit run app.py
```

3. Aplikasi akan terbuka secara otomatis di browser pada alamat:
```
http://localhost:8501
```

---

## 💡 Cara Menggunakan Aplikasi

1. Masukkan judul film yang Anda sukai ke dalam kolom input.
2. Sistem akan mencari judul film terdekat jika terdapat typo.
3. Hasil rekomendasi akan ditampilkan berdasarkan kemiripan konten.
4. Gunakan filter (tahun, rating, genre, aktor) untuk menyaring hasil.
5. Jelajahi visualisasi data untuk memahami tren film dalam dataset.

---

## 📝 Catatan Penting

- Aplikasi ini hanya menggunakan pendekatan **Content-Based**, tanpa collaborative filtering atau hybrid model.
- Sistem fuzzy matching mengandalkan **rapidfuzz** untuk akurasi pencarian judul.
- Dataset saat ini terbatas pada 300 film. Untuk performa lebih baik, Anda dapat mengganti dataset dengan jumlah film yang lebih besar.

---

## 📈 Contoh Visualisasi

- 📊 *Bar Chart*: Film dengan rating tertinggi  
- 🧩 *Pie Chart*: Distribusi genre film  
- 🕓 *Line Chart*: Tren film berdasarkan tahun rilis  

---

## 📚 Referensi

- [Scikit-learn Documentation](https://scikit-learn.org/stable/documentation.html)
- [Streamlit Documentation](https://docs.streamlit.io/)
- [Rapidfuzz (Fuzzy Matching)](https://maxbachmann.github.io/RapidFuzz/)

---

