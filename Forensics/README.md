# Forensics-101

## 📌 Deskripsi

**Forensics-101** merupakan challenge kategori **Forensics** pada Jatim Cybersecurity Competition 2026.

Pada challenge ini, peserta diberikan file:

```text
forensics-101.tar.gz
```

File tersebut berisi log percobaan login yang perlu dianalisis untuk menemukan flag yang benar.

## 🔎 Penyelesaian

### 1. Ekstrak File

Pertama, ekstrak file `forensics-101.tar.gz` untuk mendapatkan file di dalamnya.

Setelah diekstrak, terdapat file:

```text
logs.jsonl
```

### 2. Membaca Log

Untuk melihat isi dari file log, gunakan command:

```bash
cat logs.jsonl
```

Hasilnya menampilkan banyak data log dan beberapa string yang menyerupai flag.

Karena jumlah data cukup banyak, mencari flag secara manual akan kurang efisien.

### 3. Filter Menggunakan Grep

Gunakan `grep` untuk mencari baris yang mengandung format flag JCC:

```bash
grep "JCC{" logs.jsonl
```

Dengan cara ini, hasil pencarian menjadi lebih sedikit sehingga flag yang sebenarnya lebih mudah ditemukan.

### 4. Mendapatkan Flag

Setelah hasil difilter, ditemukan flag yang benar:

```text
JCC{sp0t_0n_r3g3x}
```

## 🧠 Konsep yang Dipelajari

* Log analysis
* JSONL file analysis
* Command-line investigation
* Pattern matching
* Penggunaan `grep` untuk filtering data

## 🚩 Flag

```text
JCC{sp0t_0n_r3g3x}
```
