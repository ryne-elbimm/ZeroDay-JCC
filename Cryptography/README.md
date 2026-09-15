# Crypto-101

## 📌 Deskripsi

**Crypto-101** merupakan challenge kategori **Cryptography** pada Jatim Cybersecurity Competition 2026.

Pada challenge ini, peserta diberikan sebuah file lampiran yang perlu dianalisis untuk menemukan flag. Data di dalam file menggunakan beberapa tahap encoding/enkripsi sehingga perlu diproses secara berurutan.

## 🔎 Penyelesaian

### 1. Download Lampiran

Pertama, download file lampiran yang diberikan pada challenge.

### 2. Ekstrak File

Ekstrak file dengan format `.gz` untuk mendapatkan file di dalamnya.

Setelah proses ekstraksi selesai, buka file:

```text
flag.txt
```

### 3. Decode Base64

Isi dari `flag.txt` kemudian di-decode menggunakan **Base64 Decoder**.

Proses ini menghasilkan teks yang masih perlu diproses lebih lanjut.

### 4. Caesar Cipher

Hasil dari proses Base64 kemudian diterjemahkan kembali menggunakan **Caesar Cipher**.

Setelah proses tersebut selesai, flag berhasil ditemukan.

## 🧠 Konsep yang Dipelajari

* File extraction
* Base64 decoding
* Caesar Cipher
* Analisis encoding dan cipher secara bertahap

## 🚩 Flag

```text
JCC{W3lc0me_T0_Cryp706r4phy}
```
