# 📌 Proyek SCRAPING-CITRA-SATELIT  

Proyek ini merupakan **bagian kedua** dari lima tahap utama inisiatif **SKYLEARN**:  

1. **SCRAPING-DATA-SEKOLAH**  
2. **SCRAPING-CITRA-SATELIT**  
3. **CLUSTERING-SEKOLAH**  
4. **KLASIFIKASI-SEKOLAH**  
5. **DEPLOYMENT**  

---

## 🎯 Tujuan  

Tujuan dari **SCRAPING-CITRA-SATELIT** adalah memperoleh **citra satelit bangunan sekolah** untuk **14.927 SMA di Indonesia**.  
Data sekolah (nama sekolah, kabupaten/kota, dan provinsi) yang digunakan untuk scraping dapat diperoleh dari tahap 1 (**SCRAPING-DATA-SEKOLAH**) yang dapat diakses melalui tautan berikut:  

👉 [Dataset SMA Indonesia (Google Sheets)](https://docs.google.com/spreadsheets/d/1eJ-uylcTjo_OGhcih7pgacc28KCz9Y8bx6tNw1157GM)  

Proses ini menghasilkan:  
- Citra satelit sekolah dalam format gambar  
- Koordinat geografis sekolah (**longitude** dan **latitude**)  

Data hasil scraping ini akan digunakan untuk tahap selanjutnya dalam proyek **SKYLEARN**, antara lain:  
- Analisis visual peta sebaran 14.927 sekolah SMA di Indonesia  
- Analisis clustering sekolah berbasis citra satelit  
- Klasifikasi sekolah berbasis machine learning  
- Deployment model dan aplikasi  

---

## 📂 Struktur Folder  

```
2. SCRAPING-CITRA-SATELIT/
├── data
│   └── README.md                                     # Catatan sumber data
├── hasil                                             # Hasil scraping citra satelit (gambar ori, gambar titik, gambar kotak dan yolo)
│   ├── gambar_kotak_dan_yolo
│   │   ├── ACEH
│   │   │   └── KAB ACEH BESAR
│   │   │       ├── img
│   │   │       │   ├── sma_1_pulo_aceh.jpg
│   │   │       │   ├── sma_2_lhoknga.jpg
│   │   │       │   ├── ...
│   │   │       │   └── smp_malem_putra_1.jpg
│   │   │       └── yolo
│   │   │           ├── sma_1_pulo_aceh.txt
│   │   │           ├── sma_2_lhoknga.txt
│   │   │           ├── ...
│   │   │           └── smp_malem_putra_1.txt
│   │   ├── ...
│   │   ├── ...
│   │   └── JAWA TENGAH
│   │       └── KOTA SEMARANG
│   │           ├── img
│   │           │   └── sma_negeri_1_semarang.jpg
│   │           └── yolo
│   │               └── sma_negeri_1_semarang.txt
│   ├── gambar_ori
│   │   ├── ACEH
│   │   │   └── KAB ACEH BESAR
│   │   │       ├── sma_1_pulo_aceh.jpg
│   │   │       ├── sma_2_lhoknga.jpg
│   │   │       ├── ...
│   │   │       └── smp_malem_putra_1.jpg
│   │   ├── ...
│   │   ├── ...
│   │   └── JAWA TENGAH
│   │       └── KOTA SEMARANG
│   │           └── sma_negeri_1_semarang.jpg
│   ├── gambar_titik
│   │   ├── ACEH
│   │   │   └── KAB ACEH BESAR
│   │   │       ├── sma_1_pulo_aceh.jpg
│   │   │       ├── sma_2_lhoknga.jpg
│   │   │       ├── ...
│   │   │       └── smp_malem_putra_1.jpg
│   │   ├── ...
│   │   ├── ...
│   │   └── JAWA TENGAH
│   │       └── KOTA SEMARANG
│   │           └── sma_negeri_1_semarang.jpg
│   └── tile                                            # Menyimpan potongan-potongan tile sebelum menjadi gambar utuh
│       ├── tile_200353_126975_18.jpg
│       ├── tile_200353_126976_18.jpg
│       ├── ...
│       └── tile_211477_136177_18.jpg
└── notebooks
    ├── gambar/                                         # Dokumentasi gambar untuk notebook
    └── scraping_citra_satelit.ipynb                    # Notebook untuk scraping citra satelit
```

---

## 📝 Keterangan  

1. **data/**  
   - Menyimpan data mentah atau referensi tambahan.  
   - `README.md` di dalam folder ini berisi catatan sumber data.

2. **hasil/**  
   Folder ini berisi semua hasil scraping citra satelit yang telah diproses, dibagi menjadi beberapa subfolder:  
   - **gambar_kotak_dan_yolo/**: berisi gambar sekolah dengan bounding box dan label YOLO untuk deteksi objek.  
   - **gambar_ori/**: gambar asli dari citra satelit.  
   - **gambar_titik/**: gambar citra satelit dengan titik lokasi sekolah yang ditandai.  
   - **tile/**: menyimpan potongan-potongan tile sebelum digabung menjadi citra utuh.

>⚠️ **Catatan:** Folder `hasil/` yang ada di repository hanyalah **sampel**. Apabila ingin mendapatkan hasil penuh, bisa menjalankan program sendiri atau menghubungi email: **saazizau@gmail.com** / **algaedesma2004@gmail.com**.

3. **notebooks/**  
   - **scraping_citra_satelit.ipynb**: notebook utama untuk scraping citra satelit.  
   - **gambar/**: dokumentasi gambar yang digunakan atau dihasilkan selama pengembangan notebook.  

---

## 🤝 Kolaborasi  

Proyek ini dikerjakan secara kolaboratif dalam rangka inisiatif **SKYLEARN**.  

### 👥 Kontributor  
- 🌟 **Algae Desma Fridasary** — *Ketua Tim & Visioner Utama*  
  Pemilik ide dan penggerak utama proyek. Berfokus pada penulisan artikel ilmiah serta deployment sistem.  

- 🎓 **Sabrina Aziz Aulia** — *Mentor & Spesialis Komputasi*  
  Memberikan arahan strategis dan pendampingan teknis, terutama dalam aspek komputasi dan pemodelan data.  

---

## 📢 Kontribusi  

Kami sangat terbuka untuk kontribusi dari komunitas!  
- Buat **issue** untuk melaporkan bug atau memberikan ide.  
- Ajukan **pull request** jika ingin menambahkan fitur atau perbaikan.  

> Mari bersama-sama membangun ekosistem data sekolah Indonesia yang lebih terbuka, rapi, dan bermanfaat 🚀  

