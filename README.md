# UAS_Kecerdasan-Komputasional

Apa Itu CNN (Convolutional Neural Network)? <br>
CNN adalah salah satu arsitektur deep learning yang dirancang untuk mengenali pola spasial dan temporal dalam data. <br>
CNN sangat populer untuk:<br>
Klasifikasi gambar<br>
Deteksi objek<br>
Pemrosesan teks (NLP)<br>
<br>
CNN bekerja dengan menangkap fitur lokal dari input (misalnya piksel gambar atau kata dalam teks) dan menyusunnya menjadi representasi fitur yang berguna untuk klasifikasi atau prediksi.<br>

# Komponen Utama CNN
1. Input Layer<br>
Berisi data mentah, seperti:<br>
Gambar (misalnya ukuran 28x28 piksel)<br>
Urutan teks (sudah diubah menjadi angka lewat tokenizer)<br>

2. Convolutional Layer<br>
Fungsi utama: mengekstrak fitur dari input.<br>
Menggunakan filter (kernel) kecil yang bergerak di atas input (disebut convolution).<br>
Mendeteksi pola seperti garis, tepi, bentuk, dll.<br>
Contoh:<br>
Filter 3x3 bisa mendeteksi garis horizontal/vertikal dalam gambar.<br>

3. Activation Function (ReLU)<br>
Fungsi aktivasi seperti ReLU (Rectified Linear Unit) diterapkan setelah convolution.<br>
Tujuannya:<br>
Menghilangkan nilai negatif → membuat jaringan belajar lebih cepat dan efisien.<br>

4. Pooling Layer (MaxPooling)<br>
Tujuan: mengurangi ukuran data dan menjaga fitur penting.<br>
Contoh: MaxPooling 2x2 mengambil nilai maksimum dari tiap blok 2x2.<br>
Mengurangi dimensi → mempercepat proses → mencegah overfitting.<br>

5. Flatten Layer<br>
Mengubah data 2D/3D hasil dari layer sebelumnya menjadi vektor 1D agar bisa masuk ke lapisan Dense.<br>

6. Fully Connected Layer (Dense)<br>
Menyusun semua neuron untuk memproses dan menggabungkan informasi.<br>
Biasanya terdiri dari 1 atau lebih layer Dense.<br>

7. Output Layer<br>
Untuk klasifikasi binary → 1 neuron dengan aktivasi sigmoid<br>
Untuk multi-class classification → beberapa neuron dengan softmax<br>

CNN untuk Teks (NLP)<br>
CNN juga digunakan dalam teks, terutama untuk klasifikasi seperti:<br>
Deteksi hoaks<br>
Sentiment analysis<br>
Klasifikasi topik<br>

Langkahnya:<br>
Tokenisasi teks → diubah ke urutan angka<br>
Embedding → ubah angka jadi vektor makna<br>
Conv1D → menangkap pola kata<br>
Pooling → ringkas informasi<br>
Dense → klasifikasi<br>

Kelebihan CNN:<br>
Otomatis belajar fitur penting dari data<br>
Kuat dalam mengenali pola visual/spasial<br>
Efisien dibanding metode manual (misalnya ekstraksi fitur dengan tangan)<br>

Kekurangan CNN:<br>
Membutuhkan banyak data dan waktu training<br>
Tidak ideal untuk data urutan panjang seperti kalimat panjang (lebih cocok pakai LSTM atau Transformer)
