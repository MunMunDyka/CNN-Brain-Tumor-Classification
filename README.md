# Klasifikasi Tumor Otak Menggunakan CNN  
**Andhika Laksmana - Institut Teknologi Batam**

---

## Deskripsi Proyek  
Proyek ini menggunakan Jaringan Saraf Konvolusional (CNN) untuk mengklasifikasikan tumor otak secara otomatis dari gambar MRI. Sistem ini membantu tenaga medis dalam mendeteksi dan mendiagnosis tumor otak dengan mengelompokkan hasil pemindaian MRI ke dalam dua kategori utama:  

- Tumor Terdeteksi  
- Tidak Ada Tumor  

---

## Teknologi yang Digunakan  
- **TensorFlow/Keras**: Framework deep learning untuk membangun dan melatih model CNN  
- **OpenCV**: Pemrosesan gambar MRI  
- **NumPy**: Operasi numerik dan manipulasi array  
- **Matplotlib**: Visualisasi performa model  
- **scikit-learn**: Evaluasi dan pembagian data  

---

## Arsitektur Model  
Model CNN ini terdiri dari:  
- Beberapa lapisan Conv2D dengan filter bertahap (misal 32, 64) dan aktivasi ReLU  
- Lapisan MaxPooling2D untuk reduksi dimensi  
- Lapisan Flatten untuk mengubah fitur menjadi 1D  
- Lapisan Dense dengan dropout untuk menghindari overfitting  
- Lapisan output dengan aktivasi sigmoid untuk klasifikasi biner  

---

## Cara Kerja  

### Pra-pemrosesan Gambar  
- Memuat gambar MRI otak  
- Mengubah ukuran menjadi 224x224 piksel  
- Normalisasi nilai piksel ke rentang 0-1  

### Pelatihan Model  
- Dataset dibagi menjadi training, validasi, dan testing  
- Melatih model dengan data yang sudah diproses  
- Memantau metrik akurasi dan loss  
- Menyimpan model terbaik  

### Prediksi  
- Memuat model yang sudah dilatih  
- Pra-pemrosesan gambar MRI baru  
- Melakukan prediksi kategori tumor atau tidak  

---

## Hasil  
Model mencapai akurasi sekitar:  
- Training: 95%  
- Validasi: 92%  
- Testing: 91%  

Kategori klasifikasi:  
- Tidak Ada Tumor  
- Tumor Terdeteksi  

---

## Catatan Penting  
Proyek ini untuk keperluan pembelajaran dan penelitian saja.  
Hasil prediksi tidak bisa dijadikan sebagai diagnosa medis final tanpa validasi profesional medis.  

---

## Struktur Folder  

/brain_tumor_dataset
├── tumor/ # Gambar MRI dengan tumor
└── no_tumor/ # Gambar MRI tanpa tumor

## Cara Menjalankan  
1. Install dependencies:  
   ```bash
pip install tensorflow numpy matplotlib opencv-python scikit-learn pillow
Siapkan dataset MRI otak.
Jalankan script pelatihan model.
Gunakan model untuk prediksi gambar MRI baru.