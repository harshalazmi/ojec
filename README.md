# Study Case Ojek Online

Dokumentasi ini menjelaskan struktur, fungsi, dan cara menjalankan implementasi study case Ojek Online pada folder `studycase`.

## Struktur Folder

```
studycase/
├── Ojek.java                # Class OOP untuk menghitung biaya ojek
├── MainOjek.java            # Program utama versi OOP
├── MainOjekProcedural.java  # Program utama versi procedural
└── README.md                # Dokumentasi ini
```

## Tujuan Study Case

Implementasi ini menunjukkan perbedaan antara:
- gaya **OOP (Object-Oriented Programming)**, dan
- gaya **procedural**.

Kedua versi menghitung biaya ojek online dengan aturan:
- tarif per kilometer = Rp 2500
- biaya minimum = Rp 10000
- ada perhitungan diskon mahasiswa

## Penjelasan File

### `Ojek.java`

Kelas `Ojek` adalah representasi objek untuk perjalanan ojek.

Atribut:
- `jarak` (double)
- `tarifPerKm` (double)
- `biayaMinimal` (double)

Method:
- `Ojek(double jarak)`
  - constructor untuk membuat objek Ojek dan menetapkan tarif default
- `hitungBiaya()`
  - menghitung total biaya dan membandingkan dengan `biayaMinimal`
- `setTarifPerKm(double tarifBaru)`
  - mengubah tarif per kilometer
- `diskonMahasiswa(int persen)`
  - menghitung biaya setelah potongan diskon
- `tampilkanInfo()`
  - mencetak jarak dan biaya ke layar
- `getJarak()`
  - mengambil nilai jarak untuk ditampilkan di `MainOjek`

### `MainOjek.java`

Menggunakan pendekatan OOP:
1. buat objek `Ojek` untuk dua perjalanan berbeda
2. tampilkan detail biaya masing-masing dengan `tampilkanInfo()`
3. tampilkan biaya setelah diskon mahasiswa 10%

`MainOjek.java` menampilkan bagaimana objek menyimpan data dan mendukung penggunaan kembali method.

### `MainOjekProcedural.java`

Menggunakan pendekatan procedural:
1. memanggil fungsi `tampilkanBiaya(...)` langsung dengan parameter
2. fungsi `hitungBiaya(...)` menghitung biaya berdasarkan input
3. fungsi `diskonMahasiswa(...)` menghitung diskon dari nilai biaya

Versi procedural tidak menggunakan objek, sehingga semua data ditransfer lewat parameter.

## Alur Sistematis

1. **Masukan**
   - jarak perjalanan (5.0 km dan 12.0 km)
   - tarif default 2500
   - biaya minimum 10000

2. **Proses**
   - hitung biaya = `jarak * tarifPerKm`
   - bandingkan dengan `biayaMinimal`
   - pakai nilai yang lebih besar
   - jika ada diskon, kurangi biaya sesuai persentase

3. **Keluaran**
   - jarak perjalanan
   - biaya ojek
   - biaya setelah diskon mahasiswa

## Perbedaan OOP vs Procedural

| Aspek | OOP | Procedural |
|------|-----|------------|
| Representasi data | Objek `Ojek` | Nilai parameter |
| State | Disimpan dalam objek | Tidak tersimpan |
| Fungsi | Method pada class | Fungsi static terpisah |
| Reuse | Bisa digunakan kembali dengan objek berbeda | Harus memanggil fungsi lagi |

## Cara Menjalankan

1. Buka terminal di folder `studycase`
2. Compile:

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

## Output yang Diharapkan

Versi OOP:

```
=== OJEK ONLINE JAKARTA ===
Jarak     : 5.0 km
Biaya     : Rp. 12500.0

Jarak     : 12.0 km
Biaya     : Rp. 30000.0

=== OJEK ONLINE JAKARTA (Diskon Mahasiswa 10%) ===
Jarak     : 5.0 km
Biaya     : Rp. 11250.0

Jarak     : 12.0 km
Biaya     : Rp. 27000.0
```

Versi procedural: output serupa dengan tambahan prefix `=== OJEK PROCEDURAL JAKARTA ===`.

## Catatan

- File `StudyCase.md` berisi deskripsi studi kasus dan spesifikasi.
- `README.md` ini menjelaskan struktur implementasi dan cara kerja setiap file.
- Implementasi sudah siap dijalankan selama Java terpasang.
