# BorneoStamp CLI

## Menjalankan File

Jalankan file `.bst` dengan:

```bash
bst program.bst
```

Atau menggunakan perintah `run`:

```bash
bst run program.bst
```

Contoh:

```bash
bst contoh.bst
```

---

## Bantuan

Untuk melihat daftar perintah:

```bash
bst help
```

atau:

```bash
bst --help
```

---

## Versi

Melihat versi BorneoStamp:

```bash
bst version
```

atau:

```bash
bst --version
```

Contoh hasil:

```text
BorneoStamp 0.1.0
```

---

## Memeriksa File

Untuk memeriksa file `.bst` tanpa menjalankannya:

```bash
bst check program.bst
```

Perintah ini digunakan untuk memeriksa kesalahan syntax.

Contoh:

```bash
bst check contoh.bst
```

Jika tidak ada kesalahan:

```text
File valid.
```

Jika terdapat kesalahan:

```text
Kesalahan pada baris 4:
Syntax tidak valid.
```

---

## Menampilkan Token

Untuk melihat hasil lexer:

```bash
bst tokens program.bst
```

Contoh:

```bash
bst tokens contoh.bst
```

Output dapat berisi:

```text
IDENTIFIER
ASSIGN
NUMBER
NEWLINE
TAMPILKAN
LPAREN
IDENTIFIER
RPAREN
```

Perintah ini berguna ketika melakukan debugging lexer.

---

## Menampilkan AST

Untuk melihat Abstract Syntax Tree:

```bash
bst ast program.bst
```

Contoh:

```bash
bst ast contoh.bst
```

Output:

```text
PROGRAM
├── ASSIGN
│   ├── IDENTIFIER: angka
│   └── NUMBER: 10
│
└── CALL
    ├── NAME: tampilkan
    └── ARGUMENT
        └── IDENTIFIER: angka
```

Perintah ini berguna untuk debugging parser.

---

# Perintah `run`

`run` digunakan untuk menjalankan program.

```bash
bst run program.bst
```

Contoh file:

```bst
angka = 10

tampilkan(angka)
```

Jalankan:

```bash
bst run contoh.bst
```

Hasil:

```text
10
```

---

# Perintah `check`

`check` hanya memeriksa syntax.

```bash
bst check program.bst
```

Program tidak dijalankan.

Contoh:

```bash
bst check contoh.bst
```

Jika valid:

```text
File valid.
```

---

# Perintah `tokens`

Menampilkan token yang dibuat lexer.

```bash
bst tokens program.bst
```

Digunakan untuk mengetahui bagaimana source code dibaca oleh lexer.

---

# Perintah `ast`

Menampilkan AST hasil parser.

```bash
bst ast program.bst
```

Digunakan untuk melihat struktur program setelah proses parsing.

---

# Perintah `help`

Melihat bantuan CLI:

```bash
bst help
```

Contoh:

```text
BorneoStamp CLI

Penggunaan:
  bst <file.bst>
  bst run <file.bst>
  bst check <file.bst>
  bst tokens <file.bst>
  bst ast <file.bst>
  bst help
  bst version
```

---

# Perintah `version`

Melihat versi runtime:

```bash
bst version
```

Alias:

```bash
bst --version
```

---

# Menjalankan Tanpa `run`

`run` bersifat opsional.

Keduanya dapat digunakan:

```bash
bst contoh.bst
```

dan:

```bash
bst run contoh.bst
```

Keduanya menjalankan file yang sama.

---

# Argumen File

Nama file diberikan setelah perintah.

```bash
bst run program.bst
```

Contoh dengan folder:

```bash
bst run examples/contoh.bst
```

Windows:

```powershell
bst run examples\contoh.bst
```

---

# Error File

Jika file tidak ditemukan:

```text
Tidak bisa membuka file: program.bst
```

Jika tidak memberikan file:

```bash
bst run
```

CLI menampilkan:

```text
Penggunaan:
  bst run <file.bst>
```

---

# Exit Code

CLI menggunakan exit code untuk menunjukkan hasil eksekusi.

| Exit Code | Arti                 |
| --------: | -------------------- |
|       `0` | Berhasil             |
|       `1` | Error umum           |
|       `2` | Kesalahan syntax     |
|       `3` | File tidak ditemukan |

Contoh:

```bash
bst run program.bst
```

Jika berhasil:

```text
Program selesai.
```

Exit code:

```text
0
```

---

# Struktur Perintah

Format umum:

```text
bst <perintah> <argumen>
```

Contoh:

```bash
bst run program.bst
bst check program.bst
bst tokens program.bst
bst ast program.bst
bst version
bst help
```

Format langsung:

```text
bst <file.bst>
```

Contoh:

```bash
bst program.bst
```

---

# CLI dan `pacbst`

`bst` digunakan untuk menjalankan runtime dan perintah bawaan BorneoStamp.

`pacbst` digunakan sebagai package manager.

Contoh:

```bash
bst install pacbst
```

Setelah `pacbst` tersedia:

```bash
pacbst install mathb
```

Menghapus package:

```bash
pacbst uninstall mathb
```

Mencari package:

```bash
pacbst search mathb
```

Memperbarui package:

```bash
pacbst update
```

---

# Pergantian Versi

Melihat versi yang tersedia:

```bash
pacbst versions
```

Melihat versi yang sedang digunakan:

```bash
pacbst version
```

Mengganti versi:

```bash
pacbst change version 0.1.0
```

Versi channel juga dapat digunakan:

```bash
pacbst change version stable
```

```bash
pacbst change version beta
```

```bash
pacbst change version nightly
```

---

# Ringkasan

```text
bst <file.bst>             Jalankan file
bst run <file.bst>         Jalankan file
bst check <file.bst>       Periksa syntax
bst tokens <file.bst>      Tampilkan token
bst ast <file.bst>         Tampilkan AST
bst help                   Bantuan
bst version                Versi
```

Package manager:

```text
bst install pacbst         Install pacbst

pacbst install <package>   Install package
pacbst uninstall <package> Hapus package
pacbst search <package>    Cari package
pacbst update              Update package
pacbst version             Versi pacbst
pacbst versions            Daftar versi
pacbst change version ...  Ganti versi
```
