kasus: melihat perbandingan performa dari setiap cabang di lima kota terbesar di Pulau Jawa untuk dianalisis dari segi order size, customer count, product count, brand count, dan GMV dalam basis bulanan.

Step 1: Load masing-masing data *.csv dengan Pandas

Step 2: Pengecekan dan Transformasi Data dengan melakukan, cek data sekilas (melihat bentuk data biasanya 5 data teratas), cek list kolom untuk semua dataframe apakah seluruh kolom dari keempat dataframe yang terpisah itu sama, Jika sama digabungkan. Cek informasi dataframe yang telah digabungkan, dan Statistik deskriptif dari dataframe yang telah digabungkan.

Step 3: Transformasi Data dengan cara jika ada data yang tidak seharusnya maka dapat dibuang, jika ada kolom yang seharusnya bertipe datetime64 ubahlah, cek kembali informasi dataframe, dan tampilkan kembali statistik deskriptif dari dataframe.

Step 4: Filter province yang hanya termasuk 5 provinsi besar di Jawa (DKI Jakarta, Jawa Barat, Jawa Tengah, Jawa Timur, dan Yogyakarta)

Step 5: Mengelompokkan data berdasarkan order_date dan province yang sudah difilter dan menghitung order unique count, customer unique count, product unique count, brand unique count, dan GMV (Gross Merchandise Volume = total_price untuk semua penjualan)

Step 6: Melakukan unstack untuk mendapatkan order_date di bagian baris dan province di bagian column

Step 7: Slicing data untuk masing-masing measurement (kolom), misal: kolom order

Step 8: Lakukan resampling pada data tersebut untuk dilakukan perhitungan secara bulanan

Step 9: Plot untuk hasil pada langkah #[8]

Step 10: Langah 7 s/d 9 yang telah dilakukan baru untuk satu measurement yaitu order. Berarti ada empat kali lagi kode seperti ini harus dibuat. Karena struktur code masih sama, dapat menggunakan perulangan sesuai dengan jumlah measurement yaitu 5, sehingga kelima measurement dapat ditampilkan grafiknya dalam satu canvas figure. Mari memulai dengan membuat sebuah perulangan dengan dataframe unstack_city_province yang digunakan (hasil dari langkah ke 5 di part 2).
