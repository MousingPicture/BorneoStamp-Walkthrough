# Pembelajaran Syntax

## 1. File Program

File program menggunakan ekstensi:

```text
.bst
```

Contoh:

```text
program.bst
```

Jalankan:

```text
bst run program.bst
```

atau:

```text
bst program.bst
```

---

# 2. Komentar

Komentar menggunakan `#`.

```bst
# Ini komentar

nama = "Budhi"
```

Komentar juga dapat menggunakan `//`.

```bst
// Ini komentar

angka = 10
```

Komentar tidak dijalankan sebagai kode.

---

# 3. Indentasi

Indentasi digunakan untuk menentukan isi sebuah blok kode.

```bst
jika benar
    tampilkan("Halo")
```

Kode yang berada di dalam blok harus menggunakan indentasi.

Contoh beberapa tingkat:

```bst
jika benar
    tampilkan("Level 1")

    jika benar
        tampilkan("Level 2")
```

Indentasi digunakan pada:

```text
jika
kalau tidak
selama
untuk
fungsi
```

---

# 4. Variabel

Variabel dibuat menggunakan `=`.

```bst
nama = "Budhi"
umur = 17
nilai = 95.5
```

Nilai variabel dapat diubah:

```bst
angka = 10
angka = 20
```

Variabel dapat digunakan dalam operasi:

```bst
a = 10
b = 20

hasil = a + b
```

---

# 5. String

String menggunakan tanda kutip.

```bst
nama = "Budhi"
pesan = "Halo dunia"
```

String dapat ditampilkan:

```bst
tampilkan("Halo dunia")
```

String dapat digabungkan menggunakan `+`.

```bst
bahasa = "Borneo"
hasil = bahasa + "Stamp"

tampilkan(hasil)
```

Hasil:

```text
BorneoStamp
```

---

# 6. Angka

Angka dapat berupa bilangan bulat:

```bst
umur = 17
jumlah = 100
```

atau desimal:

```bst
tinggi = 170.5
nilai = 95.5
```

---

# 7. Boolean

Nilai boolean:

```bst
benar
salah
```

Contoh:

```bst
aktif = benar
selesai = salah
```

Boolean dapat digunakan dalam kondisi:

```bst
aktif = benar

jika aktif
    tampilkan("Aktif")
```

---

# 8. Operator Aritmatika

| Operator | Contoh  | Fungsi         |
| -------- | ------- | -------------- |
| `+`      | `a + b` | Penjumlahan    |
| `-`      | `a - b` | Pengurangan    |
| `*`      | `a * b` | Perkalian      |
| `/`      | `a / b` | Pembagian      |
| `%`      | `a % b` | Sisa pembagian |

Contoh:

```bst
a = 10
b = 3

tambah = a + b
kurang = a - b
kali = a * b
bagi = a / b
sisa = a % b
```

---

# 9. Operator Perbandingan

| Operator | Arti                  |
| -------- | --------------------- |
| `==`     | Sama dengan           |
| `!=`     | Tidak sama dengan     |
| `>`      | Lebih besar           |
| `<`      | Lebih kecil           |
| `>=`     | Lebih besar atau sama |
| `<=`     | Lebih kecil atau sama |

Contoh:

```bst
umur = 18

jika umur >= 17
    tampilkan("Dewasa")
```

Contoh lain:

```bst
a = 10
b = 20

jika a < b
    tampilkan("a lebih kecil")
```

---

# 10. Operator Logika

Operator logika:

```text
dan
atau
tidak
```

Bentuk operator simbol:

```text
&&
||
!
```

Contoh:

```bst
umur = 20
memiliki_kartu = benar

jika umur >= 17 dan memiliki_kartu
    tampilkan("Syarat terpenuhi")
```

Contoh `atau`:

```bst
jika umur < 13 atau umur > 60
    tampilkan("Kelompok usia tertentu")
```

Contoh `tidak`:

```bst
aktif = benar

jika tidak aktif
    tampilkan("Tidak aktif")
```

---

# 11. Menampilkan Data

Gunakan:

```bst
tampilkan()
```

Contoh:

```bst
tampilkan("Halo")
```

Angka:

```bst
tampilkan(100)
```

Variabel:

```bst
nama = "Budhi"

tampilkan(nama)
```

Ekspresi:

```bst
a = 10
b = 20

tampilkan(a + b)
```

---

# 12. Percabangan `jika`

Syntax:

```bst
jika kondisi
    kode
```

Contoh:

```bst
nilai = 90

jika nilai >= 75
    tampilkan("Lulus")
```

---

# 13. `kalau tidak`

Digunakan untuk kondisi alternatif.

```bst
nilai = 60

jika nilai >= 75
    tampilkan("Lulus")
kalau tidak
    tampilkan("Tidak lulus")
```

---

# 14. Perulangan `selama`

Syntax:

```bst
selama kondisi
    kode
```

Contoh:

```bst
angka = 0

selama angka < 5
    tampilkan(angka)
    angka = angka + 1
```

Output:

```text
0
1
2
3
4
```

---

# 15. Perulangan `untuk`

Syntax:

```bst
untuk variabel dari awal sampai akhir
    kode
```

Contoh:

```bst
untuk angka dari 1 sampai 5
    tampilkan(angka)
```

---

# 16. Fungsi

Fungsi dibuat menggunakan `fungsi`.

```bst
fungsi halo()
    tampilkan("Halo")
```

Memanggil fungsi:

```bst
halo()
```

---

# 17. Parameter

Fungsi dapat menerima parameter.

```bst
fungsi sapa(nama)
    tampilkan(nama)
```

Pemanggilan:

```bst
sapa("Budhi")
```

Beberapa parameter:

```bst
fungsi tambah(a, b)
    tampilkan(a + b)
```

Pemanggilan:

```bst
tambah(10, 20)
```

---

# 18. `kembalikan`

Digunakan untuk mengembalikan nilai dari fungsi.

```bst
fungsi tambah(a, b)
    kembalikan a + b
```

Nilai dapat disimpan:

```bst
hasil = tambah(10, 20)

tampilkan(hasil)
```

Output:

```text
30
```

---

# 19. Fungsi dengan Kondisi

```bst
fungsi cek_nilai(nilai)
    jika nilai >= 75
        kembalikan "Lulus"
    kalau tidak
        kembalikan "Tidak lulus"
```

Pemanggilan:

```bst
hasil = cek_nilai(90)

tampilkan(hasil)
```

---

# 20. Operasi dengan Variabel

```bst
a = 10
b = 5

hasil1 = a + b
hasil2 = a - b
hasil3 = a * b
hasil4 = a / b
```

Variabel juga dapat diperbarui:

```bst
angka = 10

angka = angka + 1
```

---

# 21. Tanda Kurung

Tanda kurung digunakan untuk mengubah urutan operasi.

```bst
hasil = (10 + 5) * 2
```

Tanpa kurung:

```bst
hasil = 10 + 5 * 2
```

Dengan kurung:

```bst
hasil = (10 + 5) * 2
```

---

# 22. Prioritas Operator

Contoh:

```bst
hasil = 10 + 5 * 2
```

Perkalian dilakukan terlebih dahulu.

Hasil:

```text
20
```

Gunakan kurung jika ingin operasi tertentu dilakukan terlebih dahulu:

```bst
hasil = (10 + 5) * 2
```

Hasil:

```text
30
```

---

# 23. Ekspresi

Ekspresi dapat digunakan sebagai nilai.

```bst
hasil = 10 + 20
```

Dalam kondisi:

```bst
jika angka + 5 > 10
    tampilkan("Benar")
```

Dalam fungsi:

```bst
fungsi hitung(a, b)
    kembalikan a * b + 10
```

---

# 24. Fungsi Tanpa Parameter

```bst
fungsi mulai_program()
    tampilkan("Program dimulai")
```

Panggil:

```bst
mulai_program()
```

---

# 25. Fungsi dengan Banyak Parameter

```bst
fungsi data(nama, umur, kota)
    tampilkan(nama)
    tampilkan(umur)
    tampilkan(kota)
```

Panggil:

```bst
data("Budhi", 17, "Borneo")
```

---

# 26. Kombinasi Variabel dan Kondisi

```bst
nama = "Budhi"
umur = 18

jika umur >= 17
    tampilkan(nama)
    tampilkan("Dewasa")
kalau tidak
    tampilkan(nama)
    tampilkan("Belum dewasa")
```

---

# 27. Kombinasi Fungsi dan Perulangan

```bst
fungsi tampilkan_angka(angka)
    tampilkan(angka)

untuk angka dari 1 sampai 5
    tampilkan_angka(angka)
```

---

# 28. Program Lengkap

```bst
fungsi cek_nilai(nilai)
    jika nilai >= 75
        kembalikan "Lulus"
    kalau tidak
        kembalikan "Tidak lulus"


nama = "Budhi"
nilai = 90

hasil = cek_nilai(nilai)

tampilkan("Nama:")
tampilkan(nama)

tampilkan("Nilai:")
tampilkan(nilai)

tampilkan("Hasil:")
tampilkan(hasil)
```

Output:

```text
Nama:
Budhi
Nilai:
90
Hasil:
Lulus
```

---

# 29. Ringkasan Syntax

## Variabel

```bst
nama = "Budhi"
angka = 100
aktif = benar
```

## Komentar

```bst
# komentar
```

## Output

```bst
tampilkan("Halo")
```

## Kondisi

```bst
jika kondisi
    kode
kalau tidak
    kode
```

## Perulangan

```bst
selama kondisi
    kode
```

## Perulangan angka

```bst
untuk angka dari 1 sampai 10
    tampilkan(angka)
```

## Fungsi

```bst
fungsi nama()
    kode
```

## Parameter

```bst
fungsi tambah(a, b)
    kembalikan a + b
```

## Return

```bst
kembalikan nilai
```

## Pemanggilan fungsi

```bst
tambah(10, 20)
```
