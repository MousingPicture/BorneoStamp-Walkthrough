# Module

Module digunakan untuk menyediakan fungsi tambahan yang dapat digunakan oleh program.

Module dimuat menggunakan syntax:

```bst
dari mesin virtual pakai nama_module
```

Contoh:

```bst
dari mesin virtual pakai mathb
```

Setelah module dimuat, fungsi module dapat digunakan.

---

# 1. `mathb`

Module `mathb` menyediakan operasi matematika.

Muat module:

```bst
dari mesin virtual pakai mathb
```

---

## `mathb.tambah()`

Menjumlahkan dua angka.

```bst
hasil = mathb.tambah(10, 5)

tampilkan(hasil)
```

Hasil:

```text
15
```

---

## `mathb.kurang()`

Mengurangi angka pertama dengan angka kedua.

```bst
hasil = mathb.kurang(10, 5)

tampilkan(hasil)
```

Hasil:

```text
5
```

---

## `mathb.kali()`

Mengalikan dua angka.

```bst
hasil = mathb.kali(10, 5)

tampilkan(hasil)
```

Hasil:

```text
50
```

---

## `mathb.bagi()`

Membagi angka pertama dengan angka kedua.

```bst
hasil = mathb.bagi(10, 5)

tampilkan(hasil)
```

Hasil:

```text
2
```

Contoh pembagian:

```bst
hasil = mathb.bagi(10, 4)

tampilkan(hasil)
```

---

## `mathb.pangkat()`

Menghitung pangkat.

```bst
hasil = mathb.pangkat(2, 3)

tampilkan(hasil)
```

Hasil:

```text
8
```

---

## `mathb.akar()`

Menghitung akar kuadrat.

```bst
hasil = mathb.akar(25)

tampilkan(hasil)
```

Hasil:

```text
5
```

---

## `mathb.abs()`

Mengambil nilai absolut.

```bst
hasil = mathb.abs(-20)

tampilkan(hasil)
```

Hasil:

```text
20
```

---

## `mathb.bulat()`

Membulatkan angka.

```bst
hasil = mathb.bulat(5.7)

tampilkan(hasil)
```

Hasil:

```text
6
```

---

# 2. `tmers`

Module `tmers` digunakan untuk waktu dan penundaan program.

Muat module:

```bst
dari mesin virtual pakai tmers
```

---

## `tmers.sekarang()`

Mengambil waktu Unix saat ini.

```bst
waktu = tmers.sekarang()

tampilkan(waktu)
```

---

## `tmers.jam()`

Mengambil jam saat ini.

```bst
jam = tmers.jam()

tampilkan(jam)
```

---

## `tmers.menit()`

Mengambil menit saat ini.

```bst
menit = tmers.menit()

tampilkan(menit)
```

---

## `tmers.detik()`

Mengambil detik saat ini.

```bst
detik = tmers.detik()

tampilkan(detik)
```

---

## `tmers.tunggu()`

Menghentikan sementara program selama waktu tertentu.

Parameter menggunakan milidetik.

```bst
tmers.tunggu(1000)
```

`1000` milidetik = `1` detik.

Contoh:

```bst
tampilkan("Mulai")

tmers.tunggu(2000)

tampilkan("Selesai")
```

---

# 3. `jendelax`

Module `jendelax` digunakan untuk membuat jendela aplikasi.

Muat module:

```bst
dari mesin virtual pakai jendelax
```

---

## `jendelax.buat()`

Membuat sebuah jendela.

Format:

```bst
jendelax.buat("Judul", lebar, tinggi)
```

Contoh:

```bst
jendelax.buat("Aplikasi", 800, 600)
```

Parameter:

```text
Judul
Lebar
Tinggi
```

Contoh:

```bst
jendelax.buat(
    "Aplikasi Saya",
    800,
    600
)
```

---

## `jendelax.tampilkan()`

Menampilkan jendela yang sudah dibuat.

```bst
jendelax.buat("Aplikasi", 800, 600)

jendelax.tampilkan()
```

---

## `jendelax.tunggu()`

Menunggu sampai jendela ditutup.

```bst
jendelax.buat("Aplikasi", 800, 600)

jendelax.tampilkan()

jendelax.tunggu()
```

---

# 4. Menggunakan Beberapa Module

Beberapa module dapat digunakan dalam satu program.

```bst
dari mesin virtual pakai mathb
dari mesin virtual pakai tmers

angka = mathb.pangkat(2, 3)

tampilkan(angka)

tmers.tunggu(1000)

tampilkan("Selesai")
```

---

# 5. Module dan Fungsi

Fungsi module dapat digunakan di dalam fungsi biasa.

```bst
dari mesin virtual pakai mathb

fungsi hitung(a, b)
    kembalikan mathb.kali(a, b)

hasil = hitung(10, 5)

tampilkan(hasil)
```

---

# 6. Module dan Percabangan

```bst
dari mesin virtual pakai mathb

angka = mathb.abs(-10)

jika angka > 5
    tampilkan("Lebih besar dari 5")
kalau tidak
    tampilkan("5 atau lebih kecil")
```

---

# 7. Module dan Perulangan

```bst
dari mesin virtual pakai mathb

untuk angka dari 1 sampai 5
    hasil = mathb.pangkat(angka, 2)
    tampilkan(hasil)
```

---

# 8. Module dan Variabel

Hasil fungsi module dapat disimpan dalam variabel.

```bst
dari mesin virtual pakai mathb

a = 10
b = 20

hasil = mathb.tambah(a, b)

tampilkan(hasil)
```

---

# 9. Contoh Program dengan Semua Module

```bst
dari mesin virtual pakai mathb
dari mesin virtual pakai tmers
dari mesin virtual pakai jendelax

angka = mathb.pangkat(5, 2)

tampilkan("Hasil:")
tampilkan(angka)

tampilkan("Waktu:")
tampilkan(tmers.jam())
tampilkan(tmers.menit())
tampilkan(tmers.detik())

jendelax.buat(
    "Program",
    800,
    600
)

jendelax.tampilkan()

jendelax.tunggu()
```

---

# Daftar Module

| Module     | Kegunaan            |
| ---------- | ------------------- |
| `mathb`    | Operasi matematika  |
| `tmers`    | Waktu dan penundaan |
| `jendelax` | Jendela aplikasi    |

---

# Daftar Fungsi

## `mathb`

```text
mathb.tambah(a, b)
mathb.kurang(a, b)
mathb.kali(a, b)
mathb.bagi(a, b)
mathb.pangkat(a, b)
mathb.akar(a)
mathb.abs(a)
mathb.bulat(a)
```

## `tmers`

```text
tmers.sekarang()
tmers.jam()
tmers.menit()
tmers.detik()
tmers.tunggu(milidetik)
```

## `jendelax`

```text
jendelax.buat(judul, lebar, tinggi)
jendelax.tampilkan()
jendelax.tunggu()
```
