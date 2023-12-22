# capstone project bangkit academy 2023 batch 2
- M011BSX0624 – Felicia Natania Lingga – Padjadjaran University – Machine Learning
- M002BSY0456 – Naufal Zidan Putra Irawan – Bandung Institute of Technology – Machine Learning
- M002BSX1235 – Aliza Nurazizah Azhari – Bandung Institute of Technology – Machine Learning
- C211BSY3588 – Imam Ahmad Fahrezi – Indraprasta University – Cloud Computing
- C011BSY3833 – Muhammad Fauzan Azhiima – Padjadjaran University – Cloud Computing
- A011BSY2190 – Fakhri Fajar Ramadhan – Padjadjaran University – Mobile Development


> "Jangan tanya kenapa struktur folder dan kodenya nggak jelas, karena ini sesuai dengan slogan kami, yaitu I.S.K.Y atau *'Inkubasi Sukur Kaga Yaudah'*."

# Short Description 
This is an application to grade the user's prononciation of a word. The app has lists of words, then the user can send their prononciation of those words. The app will give if their prononciation is already right or not. 

# About the model
Kode yang disediakan adalah tentang penggunaan model Wav2Vec2, yang merupakan model pengenalan suara. Berikut adalah penjelasan rinci tentang setiap bagian dari kode:
1. **Memuat Model dan Processor Wav2Vec2**: Di awal, kode ini memuat model Wav2Vec2 yang telah dilatih sebelumnya dan processor yang terkait. Ini adalah langkah penting untuk mempersiapkan model untuk mengenali ucapan dalam audio.
2. **Menyimpan dan Memuat Model**: Bagian selanjutnya dari kode menunjukkan cara menyimpan 'state dictionary' dari model ke dalam file dan kemudian memuatnya kembali. Ini bermanfaat untuk menggunakan model yang sama di kemudian hari tanpa perlu mengulangi proses pelatihan atau pengunduhan.
3. **Konfigurasi dan Model Kustom**: Di sini, dibuat konfigurasi baru untuk model Wav2Vec2 dan diinisialisasi model baru dengan konfigurasi tersebut. Setelah itu, bobot model kustom dimuat ke dalam model ini, yang memungkinkan penggunaan model dengan pengaturan khusus atau pelatihan ulang.
4. **Pra-pemrosesan Audio**: Kode ini menggunakan `pydub` untuk menyesuaikan tingkat sampel (sampling rate) audio. Penyesuaian ini penting untuk memastikan data audio sesuai dengan format yang diharapkan oleh model.
5. **Konversi File Audio ke Array**: Menggunakan `torchaudio`, kode ini mengonversi file audio menjadi array. Array ini kemudian diproses oleh model untuk transkripsi.
6. **Fungsi Prediksi**: Fungsi `predict` dalam kode menangani konversi data audio menjadi format yang cocok untuk model, memprosesnya melalui model, dan menghasilkan transkripsi teks dari ucapan dalam audio.
7. **Menghitung Error Rate**: Bagian terakhir kode menggunakan metrik 'Character Error Rate' (CER) untuk mengevaluasi seberapa akurat model dalam mengenali teks dari audio. CER menghitung persentase kesalahan pada tingkat karakter antara teks yang dihasilkan model dengan teks asli.
