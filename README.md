# Object Recognition using SIFT

Project ini adalah implementasi **Computer Vision** untuk mendeteksi keberadaan objek tertentu dalam sebuah scene yang kompleks menggunakan algoritma **Scale-Invariant Feature Transform (SIFT)**.

## Deskripsi
Program ini bekerja dengan cara:
1. Mengekstrak fitur keypoints dari gambar1 (Rokok dengan tampilan close up).
2. Mengekstrak fitur dari gambar2 (tumpukan rokok-rokok).
3. Mencocokkan fitur menggunakan **FLANN Based Matcher**.
4. Menggunakan **Homography** untuk memetakan sudut-sudut objek gambar1 ke dalam gambar2.
5. Menggambar **Bounding Box** (kotak hijau) di sekitar objek yang ditemukan.

## Struktur Folder
- `code/`: Berisi source code utama (`object_recognition.py`).
- `dataset/`: Berisi gambar input (`gambar1.jpeg` dan `gambar2.jpeg`).
- `results/`: Tempat output gambar hasil deteksi disimpan.

## Cara Menjalankan
1. Pastikan Python dan library berikut sudah terinstall:
   pip install opencv-python numpy matplotlib

   lalu ketik:
   python code/object_recognition.py

**Ekspektasi Hasil:**
Nanti akan muncul jendela gambar baru.
* **Kiri:** Foto rokok (gambar1).
* **Kanan:** Foto tumpukan rokok-rokok.
* **Result:** Ada garis-garis penghubung, dan ada **Kotak Hijau** tebal yang membungkus rokok di foto kanan. Kalau kotak hijaunya pas/akurat, itu artinya **Object Recognition BERHASIL!**
