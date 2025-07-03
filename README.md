# UAS_Kecerdasan-Komputasional

Apa Itu CNN (Convolutional Neural Network)?
CNN adalah salah satu arsitektur deep learning yang dirancang untuk mengenali pola spasial dan temporal dalam data. CNN sangat populer untuk:
Klasifikasi gambar
Deteksi objek
Pemrosesan teks (NLP)

CNN bekerja dengan menangkap fitur lokal dari input (misalnya piksel gambar atau kata dalam teks) dan menyusunnya menjadi representasi fitur yang berguna untuk klasifikasi atau prediksi.

# Komponen Utama CNN
1. Input Layer
Berisi data mentah, seperti:
Gambar (misalnya ukuran 28x28 piksel)
Urutan teks (sudah diubah menjadi angka lewat tokenizer)

2. Convolutional Layer
Fungsi utama: mengekstrak fitur dari input.
Menggunakan filter (kernel) kecil yang bergerak di atas input (disebut convolution).
Mendeteksi pola seperti garis, tepi, bentuk, dll.
Contoh:
Filter 3x3 bisa mendeteksi garis horizontal/vertikal dalam gambar.

3. Activation Function (ReLU)
Fungsi aktivasi seperti ReLU (Rectified Linear Unit) diterapkan setelah convolution.
Tujuannya:
Menghilangkan nilai negatif → membuat jaringan belajar lebih cepat dan efisien.

4. Pooling Layer (MaxPooling)
Tujuan: mengurangi ukuran data dan menjaga fitur penting.
Contoh: MaxPooling 2x2 mengambil nilai maksimum dari tiap blok 2x2.
Mengurangi dimensi → mempercepat proses → mencegah overfitting.

5. Flatten Layer
Mengubah data 2D/3D hasil dari layer sebelumnya menjadi vektor 1D agar bisa masuk ke lapisan Dense.

6. Fully Connected Layer (Dense)
Menyusun semua neuron untuk memproses dan menggabungkan informasi.
Biasanya terdiri dari 1 atau lebih layer Dense.

7. Output Layer
Untuk klasifikasi binary → 1 neuron dengan aktivasi sigmoid
Untuk multi-class classification → beberapa neuron dengan softmax

CNN untuk Teks (NLP)
CNN juga digunakan dalam teks, terutama untuk klasifikasi seperti:
Deteksi hoaks
Sentiment analysis
Klasifikasi topik

Langkahnya:
Tokenisasi teks → diubah ke urutan angka
Embedding → ubah angka jadi vektor makna
Conv1D → menangkap pola kata
Pooling → ringkas informasi
Dense → klasifikasi

Kelebihan CNN:
Otomatis belajar fitur penting dari data
Kuat dalam mengenali pola visual/spasial
Efisien dibanding metode manual (misalnya ekstraksi fitur dengan tangan)

Kekurangan CNN:
Membutuhkan banyak data dan waktu training
Tidak ideal untuk data urutan panjang seperti kalimat panjang (lebih cocok pakai LSTM atau Transformer)
