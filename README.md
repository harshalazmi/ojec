# Praktikum Ojek Online

Dokumentasi ini menyajikan implementasi study case Ojek Online dengan dua gaya pemrograman:
- **Gaya OOP** pada `MainOjek.java` dan `Ojek.java`
- **Gaya Procedural** pada `MainOjekProcedural.java`

## 📁 Struktur Folder

```
studycase/
├── Ojek.java                # Kelas OOP untuk menghitung biaya ojek
├── MainOjek.java            # Program utama versi OOP
├── MainOjekProcedural.java  # Program utama versi procedural
├── StudyCase.md             # Penjelasan studi kasus
├── README.md                # Dokumentasi utama study case
└── readme2.md               # Dokumentasi tambahan ini
```

## 🎯 Tujuan Study Case

Tujuan dari study case ini adalah memperlihatkan perbedaan antara:
- **Object-Oriented Programming (OOP)**
- **Gaya Procedural**

Keduanya menghitung biaya ojek online berdasarkan aturan:
- tarif per kilometer = Rp 2500
- biaya minimum = Rp 10000
- mendukung diskon mahasiswa

## 📌 Penjelasan Implementasi

### `Ojek.java`

Kelas ini menyimpan data perjalanan dan menghitung biaya ojek.

Fitur utama:
- `hitungBiaya()` menghitung total biaya dan menerapkan biaya minimum
- `diskonMahasiswa(int persen)` menghitung biaya setelah diskon
- `tampilkanInfo()` mencetak detail perjalanan
- `setTarifPerKm(double tarifBaru)` mengubah tarif per km

### `MainOjek.java`

Implementasi gaya OOP:
- membuat objek `Ojek`
- memanggil method untuk menghitung dan menampilkan biaya
- memanfaatkan ulang objek untuk berbagai perjalanan

### `MainOjekProcedural.java`

Implementasi gaya procedural:
- menggunakan fungsi static di luar objek
- semua data dilempar sebagai parameter
- tidak ada state tersimpan di dalam objek

## 🧠 Perbedaan OOP vs Procedural

| Aspek | OOP | Procedural |
|------|-----|------------|
| Representasi data | Objek `Ojek` | Parameter fungsi |
| State | Disimpan pada objek | Tidak tersimpan |
| Reuse | Method dalam objek bisa dipakai ulang | Fungsi dipanggil ulang |
| Struktur | Lebih modular | Lebih linear |

## ▶️ Cara Menjalankan

1. Buka terminal di folder `studycase`
2. Compile semua file Java:

```bash
javac Ojek.java MainOjek.java MainOjekProcedural.java
```

3. Jalankan versi OOP:

```bash
java MainOjek
```

4. Jalankan versi procedural:

```bash
java MainOjekProcedural
```

## ✅ Output yang Diharapkan

Versi OOP akan menampilkan data jarak, biaya, dan biaya setelah diskon mahasiswa.
Versi procedural menampilkan hasil serupa dengan gaya pemanggilan fungsi langsung.

## 📝 Catatan

- `StudyCase.md` berisi deskripsi studi kasus dan aturan perhitungan.
- `README.md` di folder `studycase` menjelaskan struktur implementasi dan perbedaan OOP/procedural.
- `readme2.md` ini menyajikan dokumentasi tambahan yang mengikuti gaya dokumentasi `README.md` di folder utama.
