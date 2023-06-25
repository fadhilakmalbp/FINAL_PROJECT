# FINAL_PROJECT
UAS Deep Learning Kelompok 1


Nama Penanggung Jawab: Muhammad Fadhil Akmal B. Paloloang (F55120019)

Kelompok 1:
1. Ahmad Mustamin (F55120006)
2. Nurul Fajriyah (F55120011)
3. Tri Krama (F55120014)
4. Muhammad Alif Fatharani (F55120015)
5. Muhammad Fadhil Akmal B. Paloloang (F55120019)

Penjelasan Program :
Program ini bertujuan untuk melakukan Multiclass Calssification menggunakan Transfer learning VGG-16. Program diawali dengan menginstall beberapa Library dan package yang akan digunakan seperti TensorFlow, NumPy, Pandas, Matplotlib, PIL (Python Imaging Library), OpenCV, dan sebagainya.
- Mount Google Drive: Kode ini menggunakan Google Colab, sehingga perlu melakukan mount ke Google Drive untuk mengakses dataset yang disimpan di sana.
- ImageDataGenerator: Kode ini menggunakan ImageDataGenerator dari TensorFlow untuk melakukan augmentasi data pada gambar-gambar dalam dataset. Augmentasi data dilakukan untuk meningkatkan variasi data pelatihan dan menghindari overfitting.
- Generate Data: Fungsi ini menggunakan ImageDataGenerator untuk membuat generator data pelatihan dan validasi. Generator ini akan menghasilkan batch-batch gambar yang telah diubah ukurannya, dinormalisasi, dan mengikuti konfigurasi augmentasi yang telah ditentukan.
- Model VGG16: Kode ini menggunakan arsitektur VGG16 sebagai model dasar. VGG16 adalah model jaringan saraf konvolusi yang telah dilatih sebelumnya dengan dataset ImageNet. Di sini, kita mengambil bagian dari model VGG16 yang bertanggung jawab untuk ekstraksi fitur dan menambahkan beberapa lapisan tambahan di atasnya.
- Definisi Output: Kode ini mendefinisikan lapisan-lapisan keluaran untuk model. Model ini akan memiliki dua keluaran: keluaran untuk klasifikasi gender (binary) dan keluaran untuk klasifikasi tipe orang (multiclass).
- Kompilasi Model: Model ini dikompilasi dengan fungsi kerugian dan pengoptimal yang sesuai untuk masing-masing keluaran. Juga ditentukan metrik evaluasi yang ingin digunakan, dalam hal ini akurasi.
- Pelatihan Model: Model dilatih dengan menggunakan generator data pelatihan dan validasi yang telah dibuat sebelumnya. Pelatihan dilakukan dengan menggunakan metode fit() dari TensorFlow.
- Visualisasi Hasil: Setelah pelatihan selesai, grafik untuk akurasi dan kerugian model pada set pelatihan dan validasi akan ditampilkan menggunakan Matplotlib.
- terakhir ialah melakukan testing menggunakan gambar baru untuk melakukan prediksi.

Link Dataset : https://drive.google.com/drive/folders/1wQMXJTqbcFBWMueADdJyVG6TawFJfg8t

Cara Menjalankan :
- Import library yang diperlukan.
- Lakukan mount Google Drive menggunakan drive.mount('/content/gdrive').
- Tentukan direktori pelatihan dan validasi.
- Buat generator data pelatihan dan validasi menggunakan fungsi generate_data(DIR) dengan argumen direktori pelatihan dan validasi.
- Set konfigurasi model dan arsitektur menggunakan model VGG16.
- Tentukan lapisan keluaran untuk klasifikasi gender dan klasifikasi tipe orang.
- Kompilasi model dengan fungsi kerugian, pengoptimal, dan metrik evaluasi yang sesuai.
- Tentukan callback untuk menyimpan model terbaik dan menghentikan pelatihan jika terjadi overfitting.
- Latih model menggunakan fungsi fit() dengan argumen generator data pelatihan, generator data validasi, jumlah epoch, dan callback.
- Tampilkan grafik akurasi dan kerugian model pada set pelatihan dan validasi menggunakan Matplotlib.
