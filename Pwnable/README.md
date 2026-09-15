# Pwn-101

## 📌 Deskripsi

Pada challenge **Pwn-101**, peserta diberikan sebuah service yang dapat diakses melalui koneksi remote menggunakan `nc HOST 9000` atau `ncat` bagi pengguna Windows.

Selain service tersebut, peserta juga diberikan file `pwn-101.tar.gz` untuk dianalisis secara lokal. Setelah file diekstrak, terdapat source code `chall.c` yang digunakan untuk memahami cara kerja program.

## 🔎 Analisis Source Code

Setelah membuka `chall.c`, terdapat beberapa bagian penting pada program:

* **Global variable** digunakan untuk menyimpan isi dari `flag.txt`.
* Program menggunakan `signal(SIGSEGV, crash_handler)` untuk menangani kondisi `SIGSEGV`.
* Fungsi `crash_handler` membaca `flag.txt` kemudian mencetak isinya.
* Program menggunakan fungsi `gets(name)` dengan buffer berukuran 256 karakter.
* Fungsi `gets()` tidak membatasi jumlah karakter yang dimasukkan sehingga memungkinkan terjadinya **buffer overflow**.

## 💥 Penyelesaian

Karena buffer `name` memiliki kapasitas 256 karakter dan input tidak dibatasi, program dapat mengalami **buffer overflow** apabila diberikan input yang lebih panjang dari kapasitas tersebut.

Input berupa karakter random, misalnya `A`, diberikan dalam jumlah lebih dari 256 karakter hingga program mengalami crash atau `Segmentation Fault`.

Crash tersebut memicu `SIGSEGV` sehingga `crash_handler` dijalankan dan isi `flag.txt` ditampilkan.

## 🧠 Konsep yang Dipelajari

* Buffer Overflow
* Stack Memory
* Segmentation Fault (`SIGSEGV`)
* Unsafe function `gets()`
* Signal Handler

## 🚩 Flag

```text
JCC{Buff3r_0v3rfl0w_1s_D4n63r0us!}
```
