PENJELASAN STUDI KASUS:

# Fungsi Faktorial Rekursif

## Deskripsi
Program ini dirancang untuk menghitung faktorial dari sebuah bilangan bulat dengan menggunakan metode rekursif. Faktorial dari suatu bilangan n, yang ditulis sebagai n!, adalah hasil perkalian dari n hingga 1. Sebagai contoh, faktorial dari 6 adalah 6 × 5 × 4 × 3 × 2 × 1, yang hasilnya adalah 720.

## Manfaat Penggunaan Fungsi
- **Modularitas:** Dengan menggunakan fungsi, kita dapat membagi program menjadi bagian-bagian kecil yang lebih mudah dikelola dan dipahami.
- **Reusabilitas:** Fungsi yang sudah dibuat dapat digunakan kembali di berbagai bagian program tanpa perlu menulis ulang kode.
- **Abstraksi:** Pengguna fungsi tidak perlu mengetahui detail implementasi, cukup tahu cara memanggil fungsi tersebut.
- **Pemeliharaan dan Pengujian:** Memudahkan dalam menemukan dan memperbaiki kesalahan, karena setiap fungsi dapat diuji secara terpisah.

## Cara Kerja Rekursi dalam Menghitung Faktorial
Rekursi adalah teknik di mana sebuah fungsi memanggil dirinya sendiri untuk menyelesaikan masalah. Dalam program ini, fungsi `factorial(n)` memiliki dua kondisi:

1. **Kasus Dasar:** Jika `n` adalah 0 atau 1, fungsi akan mengembalikan nilai 1. Ini adalah titik akhir dari proses rekursi, yang mencegah pemanggilan fungsi yang tidak terbatas.
2. **Kasus Rekursif:** Jika `n` lebih besar dari 1, fungsi akan memanggil dirinya sendiri dengan parameter `n - 1` dan mengalikan hasilnya dengan `n`. Dengan kata lain, untuk menghitung n!, kita perlu menghitung (n-1)! terlebih dahulu.

Sebagai contoh, jika kita ingin menghitung faktorial dari 6 (6!):
6! = 6 × 5! 5! = 5 × 4! 4! = 4 × 3! 3! = 3 × 2! 2! = 2 × 1! 1! = 1 (ini adalah kasus dasar)
Setelah mencapai kasus dasar, fungsi akan mulai mengembalikan hasil ke atas, sehingga kita mendapatkan:
6! = 6 × 5 × 4 × 3 × 2 × 1 = 720
Metode rekursif ini memberikan cara yang elegan dan terstruktur untuk menghitung faktorial.

## Cara Menggunakan Program
Untuk menggunakan program ini, jalankan program dan masukkan angka bulat yang ingin dihitung faktorialnya.

Contoh output yang akan ditampilkan:
Masukkan angka untuk menghitung faktorial: 6 Faktorial dari 6 adalah 720

Jika Anda memasukkan angka negatif atau bukan bilangan bulat, program akan memberikan pesan peringatan yang sesuai.

PENJELASAN STUDI KASUS KASUS: PENJELASAN PENGGUNAAN PERULANGAN DAN ARRAY DALAM SISTEM INPUT NILAI SISWA DAN MENCARI NILAI TERTINGGI

# Sistem Input Nilai Siswa

## Deskripsi
Program ini dibuat untuk membantu guru dalam mengumpulkan dan mencari nilai tertinggi dari 5 siswa. Pengguna akan diminta untuk memasukkan nilai satu per satu, dan program akan memastikan bahwa nilai yang dimasukkan berada dalam rentang yang benar, yaitu antara 0 hingga 100. Setelah semua nilai dimasukkan, program akan menampilkan nilai tertinggi dan siswa yang mendapat nilai tersebut.

## Penggunaan Perulangan
Program ini menggunakan perulangan untuk dua tujuan utama:

1. **Mengumpulkan Input Nilai Siswa**:
   - Dengan menggunakan `for i in range(5):`, program mengulangi proses pengambilan input sebanyak 5 kali, sesuai dengan jumlah siswa. Setiap iterasi mewakili satu siswa.
   - Di dalam perulangan, terdapat `while True:` yang menciptakan loop tak terbatas untuk memastikan bahwa input yang dimasukkan valid. Jika input tidak sesuai, program akan meminta pengguna untuk mencoba lagi.

2. **Validasi Input**:
   - Di dalam loop `while`, kita menggunakan blok `try` dan `except` untuk menangani kesalahan saat mengonversi input menjadi angka. Jika pengguna memasukkan nilai yang tidak valid, program akan memberikan pesan kesalahan dan meminta input ulang tanpa menghentikan program.

## Penggunaan Array (List)
Array, yang dalam Python disebut list, digunakan untuk menyimpan nilai-nilai yang dimasukkan oleh pengguna. Berikut adalah cara penggunaannya:

1. **Menyimpan Nilai Siswa**:
   - `nilai_siswa = []` adalah list kosong yang digunakan untuk menyimpan nilai dari 5 siswa. Setiap kali pengguna memasukkan nilai yang valid, nilai tersebut ditambahkan ke dalam list menggunakan `nilai_siswa.append(nilai)`.

2. **Mencari Nilai Tertinggi**:
   - Setelah semua nilai siswa dimasukkan, kita menggunakan fungsi `max(nilai_siswa)` untuk menemukan nilai tertinggi di dalam list.
   - Untuk mengetahui siswa mana yang memiliki nilai tertinggi, kita menggunakan `nilai_siswa.index(nilai_tertinggi) + 1`, yang mengembalikan indeks dari nilai tertinggi dan menyesuaikannya dengan nomor siswa.

## Contoh Penggunaan
Saat program dijalankan, pengguna akan diminta untuk memasukkan nilai siswa. Berikut adalah contoh interaksi:
Masukkan nilai 5 siswa: Nilai siswa ke-1: 99 Nilai siswa ke-2: 88 Nilai siswa ke-3: 77 Nilai siswa ke-4: 66 Nilai siswa ke-5: 55 Nilai tertinggi adalah 99.0 yang diperoleh siswa ke-1.

Jika input tidak valid, program akan memberikan pesan kesalahan dan meminta input ulang.

## Kesimpulan
Dengan menggunakan perulangan dan array, program ini dapat mengumpulkan, menyimpan, dan memproses data nilai siswa dengan efisien. Penggunaan kedua konsep ini sangat penting dalam pemrograman untuk menangani data secara efektif dan membuat program lebih terstruktur serta mudah dikelola.

PENJELASAN STUDI KASUS:

# Sistem Diskon E-Commerce

## Deskripsi
Program ini dirancang untuk menghitung total bayar pelanggan dalam sistem e-commerce, dengan memberikan diskon 10% jika total belanja melebihi Rp500.000. Program ini akan meminta pengguna untuk memasukkan total belanja dan kemudian menghitung total bayar setelah mempertimbangkan diskon yang berlaku.

## Struktur Kontrol Percabangan

Program ini menggunakan struktur kontrol percabangan untuk menentukan apakah pelanggan berhak mendapatkan diskon berdasarkan total belanja mereka. Berikut adalah penjelasan mengenai penggunaannya:

1. **Pernyataan `if`**:
   - Program memeriksa apakah total belanja pelanggan lebih dari Rp500.000 dengan menggunakan pernyataan `if`:
     ```python
     if total_belanja > 500000:
     ```
   - Jika kondisi ini benar (true), maka blok kode di dalam pernyataan `if` akan dieksekusi, yang berarti pelanggan berhak mendapatkan diskon.

2. **Menghitung Diskon dan Total Bayar**:
   - Jika pelanggan memenuhi syarat untuk mendapatkan diskon, program menghitung jumlah diskon dengan mengalikan total belanja dengan 10% (0.10):
     ```python
     diskon = total_belanja * 0.10
     ```
   - Total bayar setelah diskon dihitung dengan mengurangkan jumlah diskon dari total belanja:
     ```python
     total_bayar = total_belanja - diskon
     ```
   - Program kemudian mencetak pesan yang memberitahukan pelanggan bahwa mereka mendapatkan diskon dan menampilkan total bayar setelah diskon.

3. **Blok `else`**:
   - Jika kondisi dalam pernyataan `if` tidak terpenuhi (total belanja kurang dari atau sama dengan Rp500.000), maka blok `else` akan dieksekusi:
     ```python
     else:
         print(f"Total bayar: Rp{total_belanja:.2f}")
     ```
   - Dalam blok ini, program hanya mencetak total bayar tanpa diskon, karena pelanggan tidak memenuhi syarat untuk mendapatkan diskon.

4. **Penanganan Kesalahan Input**:
   - Program juga menggunakan blok `try` dan `except` untuk menangani kemungkinan kesalahan saat pengguna memasukkan total belanja. Jika input tidak valid (misalnya, bukan angka), program akan mencetak pesan kesalahan:
     ```python
     except ValueError:
         print("Input tidak valid. Harap masukkan angka.")
     ```

## Contoh Penggunaan
Saat program dijalankan, pengguna akan diminta untuk memasukkan total belanja. Berikut adalah contoh interaksi:
Masukkan total belanja: Rp599999 Anda mendapatkan diskon 10%. Total bayar setelah diskon: Rp539999.10

Jika input tidak valid, program akan memberikan pesan kesalahan dan meminta input ulang.

## Kesimpulan
Dengan menggunakan struktur kontrol percabangan, program ini dapat menentukan dengan jelas apakah pelanggan berhak mendapatkan diskon dan menghitung total bayar yang sesuai. Ini membuat logika program menjadi terstruktur dan memberikan pengalaman pengguna yang baik dengan memberikan informasi yang tepat berdasarkan input yang diberikan.

PENJELASAN STUDI KASUS: 

# Program Menghitung Total Harga Pembelian 3 Barang

## Deskripsi
Program ini dirancang untuk membantu kasir toko dalam menghitung total harga pembelian dari 3 barang. Pengguna akan diminta untuk memasukkan harga masing-masing barang, dan program akan menghitung serta menampilkan total harga yang harus dibayar.

## Langkah-langkah Algoritma
1. **Mulai Program**: Program dimulai dan siap untuk dijalankan.
2. **Tampilkan Judul Program**: Menampilkan pesan yang menjelaskan fungsi program.
3. **Input Harga Barang**:
   - Meminta pengguna untuk memasukkan harga barang 1.
   - Meminta pengguna untuk memasukkan harga barang 2.
   - Meminta pengguna untuk memasukkan harga barang 3.
4. **Validasi Input**: Memastikan bahwa input yang dimasukkan adalah angka. Jika tidak, program akan menampilkan pesan kesalahan.
5. **Hitung Total Harga**: Menjumlahkan harga barang untuk mendapatkan total.
6. **Tampilkan Total Harga**: Menampilkan total harga dengan format yang rapi.
7. **Selesai**: Program berakhir setelah menampilkan total harga.

## Cara Menggunakan
1. Jalankan program menggunakan Python.
2. Masukkan harga untuk 3 barang ketika diminta.
3. Program akan menghitung dan menampilkan total harga yang harus dibayar.

## Contoh
Jika pengguna memasukkan harga:
- Barang 1: Rp 100.000
- Barang 2: Rp 2.500.000
- Barang 3: Rp 1.500.000

Maka output yang dihasilkan adalah:
Total harga yang harus dibayar: Rp 4,100,000.00

## Catatan
- Pastikan untuk memasukkan harga dalam format angka yang benar.
- Program ini menggunakan pemisah ribuan dan dua angka desimal untuk menampilkan total harga.

PENJELASAN STUDI KASUS: 

# Program Menentukan Status Kelulusan Siswa

## Deskripsi
Program ini dirancang untuk membantu siswa mengetahui apakah nilai ujiannya memenuhi syarat lulus berdasarkan rata-rata nilai dari 3 mata pelajaran. Jika rata-rata nilai ≥ 75, siswa dinyatakan lulus; jika tidak, siswa dinyatakan tidak lulus.

## Cara Kerja Program
1. **Memulai Program**: Program dimulai dengan menampilkan pesan yang menjelaskan fungsinya.
2. **Input Nilai**: Pengguna diminta untuk memasukkan nilai dari 3 mata pelajaran. Nilai yang dimasukkan harus berupa angka.
3. **Validasi Input**: Program menggunakan blok `try-except` untuk memastikan bahwa input yang dimasukkan adalah angka. Jika pengguna memasukkan nilai yang bukan angka, program akan menampilkan pesan kesalahan dan berhenti.
4. **Menghitung Rata-rata**: Program menjumlahkan ketiga nilai yang dimasukkan dan membaginya dengan 3 untuk mendapatkan rata-rata.
5. **Menampilkan Rata-rata**: Program menampilkan rata-rata nilai dengan format dua angka desimal.
6. **Menentukan Status Kelulusan**: Program membandingkan rata-rata nilai dengan angka 75. Jika rata-rata lebih besar atau sama dengan 75, program akan menampilkan "Status: Lulus". Jika tidak, program akan menampilkan "Status: Tidak Lulus".

## Contoh Penggunaan
Jika siswa memasukkan nilai sebagai berikut:
- Mata Pelajaran 1: 80
- Mata Pelajaran 2: 75
- Mata Pelajaran 3: 70

Maka output yang dihasilkan adalah:
Rata-rata nilai: 75.00 Status: Lulus

## Catatan
- Pastikan untuk memasukkan nilai dalam format angka yang benar.
- Program ini menggunakan dua angka desimal untuk menampilkan rata-rata nilai.
