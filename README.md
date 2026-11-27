# LAPORAN ALGORITMA
## MEMBANDINGKAN 3 ALGORITMA
**Nama Kelompok :** Kelompok 6 <br>
**Kelas :** 3B <br>
**Anggota Kelompok :** 
1. Tiara Sasa Sabilah (1251170073)
2. Nurul Adzani (1251170135)
3. Berlin Ghea Yuliant (1251170142)
4. Aulia Rahmawaty (1251170143)
5. Nayla Dwi Maharani (1251170145)
6. Hisyam Habiburahman (1251170170)

# Perbandingan Bubble Sort, Merge Sort, dan Quick Sort

## 1. Tujuan
Laporan ini membandingkan tiga algoritma untuk mengurutkan angka dari yang
terkecil ke terbesar:
  1. Bubble Sort
  2. Merge Sort
  3. Quick Sort
Ketiganya menerima jenis data dan ukuran data yang sama. Kita memeriksa apakah hasilnya benar, lalu membandingkan waktu yang dibutuhkan.

## 2. Contoh Cara Kerja
Misalkan angka yang akan diurutkan adalah:
```text
5, 3, 8, 1, 2
```
Hasil akhirnya untuk ketiga algoritma harus sama:
```text
1, 2, 3, 5, 8
```

### A. Bubble Sort
Bandingkan angka yang bersebelahan. Tukar posisinya jika angka kiri lebih besar.
Ulangi dari kiri sampai kanan beberapa kali.

```text
Awal       : 5, 3, 8, 1, 2
Putaran 1  : 3, 5, 1, 2, 8
Putaran 2  : 3, 1, 2, 5, 8
Putaran 3  : 1, 2, 3, 5, 8
Hasil      : 1, 2, 3, 5, 8
```

Contoh: pada langkah pertama, `5` dibandingkan dengan `3`. Karena `5` lebih
besar, keduanya ditukar.

### B. Merge Sort
Bagi data menjadi bagian-bagian kecil sampai tiap bagian tinggal satu angka.
Lalu gabungkan kembali sambil menaruh angka dalam urutan yang benar.

```text
Mulai       : [5, 3, 8, 1, 2]
Dibagi      : [5, 3, 8] dan [1, 2]
Dibagi lagi : [5, 3] [8] dan [1] [2]
Digabung    : [3, 5] [8] dan [1, 2]
Hasil       : [1, 2, 3, 5, 8]
```

### C. Quick Sort
Pilih satu angka sebagai **pivot**. Pindahkan angka yang lebih kecil ke kiri
pivot dan angka yang lebih besar ke kanan. Lakukan lagi pada bagian kiri dan
kanan sampai urut.
```text
Mulai                 : [5, 3, 8, 1, 2]
Pivot pertama (2)     : [1] [2] [5, 3, 8]
Urutkan bagian kanan  : [3] [5] [8]
Hasil                 : [1, 2, 3, 5, 8]
```
Kode contoh memilih angka terakhir pada bagian yang sedang diproses sebagai
pivot.

## 3. Metode Pengujian
- Ukuran data: 1.000, 2.500, 4.000, dan 5.000 angka.
- Angka dibuat secara acak.
- Setiap ukuran diuji 5 kali; waktu yang dicatat adalah rata-ratanya.
- Semua program memakai ukuran data, cara membuat angka, dan timer yang sama.
- Program mencetak `OK` jika angka setelah sorting sudah urut.
- Waktu diukur dengan fungsi `clock()` dari bahasa C.

Kompilasi menggunakan GCC atau MinGW:
```text
gcc -O2 bubble_sort.c -o bubble_sort.exe
gcc -O2 merge_sort.c -o merge_sort.exe
gcc -O2 quick_sort.c -o quick_sort.exe
```

Jalankan satu per satu:
```text
bubble_sort.exe
merge_sort.exe
quick_sort.exe
```
Program mencetak CSV. Salin kolom `waktu_rata2_detik` ke tabel hasil. Jalankan
semua program di komputer yang sama agar perbandingannya adil.

## 4. Hasil Pengujian
Isi tanda `-` dari hasil menjalankan program. Jangan isi dengan angka tebakan,
karena waktu tergantung pada komputer yang digunakan.

| Jumlah angka | Bubble Sort (detik) | Merge Sort (detik) | Quick Sort (detik) | Status hasil |
|---:|---:|---:|---:|:---:|
| 1.000 | - | - | - | - |
| 2.500 | - | - | - | - |
| 4.000 | - | - | - | - |
| 5.000 | - | - | - | - |

`Status hasil` diisi `OK` jika ketiga program berhasil mengurutkan data.

## 5. Grafik Perbandingan
Buat grafik garis berdasarkan tabel hasil:
- Sumbu X: jumlah angka.
- Sumbu Y: waktu rata-rata dalam detik.
- Garis 1: Bubble Sort.
- Garis 2: Merge Sort.
- Garis 3: Quick Sort.
- Judul: **Perbandingan Waktu Tiga Algoritma Sorting**.

Cara membuatnya di Excel atau LibreOffice Calc:
1. Masukkan data dari tabel hasil.
2. Pilih kolom jumlah angka dan kolom waktu ketiga algoritma.
3. Pilih **Insert/Sisipkan → Chart/Bagan → Line/Garis**.
4. Tempelkan grafik di bawah ini.

> Tempelkan grafik dari hasil pengujian di sini.

## 6. Perbandingan Sederhana
| Algoritma | Kecepatan teori | Memori tambahan | Penjelasan singkat |
|---|---|---|---|
| Bubble Sort | Lambat untuk data banyak: O(n^2) | Sedikit: O(1) | Paling mudah dilihat langkah-langkahnya |
| Merge Sort | Cepat dan stabil: O(n log n) | Lebih banyak: O(n) | Membagi data lalu menggabungkannya |
| Quick Sort | Biasanya cepat: O(n log n) rata-rata | Sedikit pada umumnya | Memisahkan data memakai pivot |

`n` berarti jumlah angka. O(n^2) biasanya bertambah lebih cepat daripada
O(n log n) saat jumlah data membesar. Quick Sort bisa menjadi O(n^2) pada kasus
terburuk, misalnya jika pembagian pivot terus tidak seimbang.

## 7. Analisis dan Kesimpulan

Isi berdasarkan tabel dan grafik yang sudah dibuat:

- Waktu tercepat pada pengujian ini: **........................**
- Waktu terlambat pada pengujian ini: **........................**
- Apakah semua hasil menunjukkan `OK`? **........................**

Secara umum, Bubble Sort mudah dipahami tetapi kurang cocok untuk data besar.
Merge Sort dan Quick Sort biasanya lebih cepat ketika jumlah data banyak.
Kesimpulan akhir tetap harus mengikuti hasil pengukuran pada komputer yang
digunakan.

## 8. Rekomendasi
- Gunakan **Bubble Sort** untuk memahami dasar sorting dan latihan dengan data
  sedikit.
- Gunakan **Merge Sort** jika ingin waktu yang konsisten dan tidak keberatan
  memakai memori tambahan.
- Gunakan **Quick Sort** jika menginginkan sorting yang biasanya cepat dan
  penggunaan memori tambahan yang relatif kecil.

## 9. Berkas Program
- `bubble_sort.c` — program pengujian Bubble Sort.
- `merge_sort.c` — program pengujian Merge Sort.
- `quick_sort.c` — program pengujian Quick Sort.

