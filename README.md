# Sistem Perpustakaan Laravel

## Identitas

| Keterangan | Data |
|------------|------|
| Nama | Said Fachri Ariza |
| NIM | [60324023] |


---

## Deskripsi Proyek

Proyek ini merupakan implementasi aplikasi Sistem Perpustakaan menggunakan framework Laravel. Sistem dikembangkan dengan menerapkan konsep MVC (Model-View-Controller), Routing, Migration, Model, Seeder, dan Blade Template.

Aplikasi ini digunakan untuk mengelola data anggota perpustakaan dan kategori buku secara terstruktur sesuai prinsip normalisasi database.

---

## Fitur yang Diimplementasikan

### 1. Routing dan View Anggota

- Menampilkan daftar anggota perpustakaan
- Menampilkan detail anggota berdasarkan ID
- Menggunakan Blade Template
- Menggunakan Bootstrap 5

Route:

```php
/anggota
/anggota/{id}
```

---

### 2. Controller Kategori

Controller:

```php
KategoriController
```

Method:

- index()
- show($id)
- search($keyword)

Route:

```php
/kategori
/kategori/{id}
/kategori/search/{keyword}
```

---

### 3. Layout Master

Menggunakan layout utama:

```txt
resources/views/layouts/app.blade.php
```

Fitur:

- Navbar Bootstrap
- Template inheritance menggunakan Blade
- Named Routes

---

### 4. Database Migration

Tabel:

```txt
kategori
```

Struktur:

| Field | Tipe |
|---------|---------|
| id | bigint |
| nama_kategori | varchar(50) |
| deskripsi | text |
| icon | varchar(50) |
| warna | varchar(20) |
| created_at | timestamp |
| updated_at | timestamp |

---

### 5. Model

Model:

```php
Kategori
```

Fillable:

```php
nama_kategori
deskripsi
icon
warna
```

---

### 6. Seeder

Data awal kategori:

1. Programming
2. Database
3. Web Design
4. Networking
5. Data Science

---

## Struktur Folder

```txt
app
├── Http
│   └── Controllers
│       └── KategoriController.php
│
└── Models
    └── Kategori.php

database
├── migrations
│   └── create_kategori_table.php
│
└── seeders
    ├── DatabaseSeeder.php
    └── KategoriSeeder.php

resources
└── views
    ├── layouts
    │   └── app.blade.php
    │
    ├── anggota
    │   ├── index.blade.php
    │   └── show.blade.php
    │
    └── kategori
        ├── index.blade.php
        ├── show.blade.php
        └── search.blade.php

routes
└── web.php
```

---

## Cara Menjalankan

Clone repository:

```bash
git clone <url-repository>
```

Masuk ke folder project:

```bash
cd perpustakaan
```

Install dependency:

```bash
composer install
```

Copy file environment:

```bash
cp .env.example .env
```

Generate application key:

```bash
php artisan key:generate
```

Jalankan migration:

```bash
php artisan migrate
```

Jalankan seeder:

```bash
php artisan db:seed
```

Menjalankan aplikasi:

```bash
php artisan serve
```

Buka browser:

```txt
http://127.0.0.1:8000
```

---

## Teknologi yang Digunakan

- Laravel
- PHP
- MySQL
- Bootstrap 5
- Blade Template
- Eloquent ORM

---

## Hasil

Aplikasi berhasil mengimplementasikan:

- Routing Laravel
- Controller MVC
- Blade Template
- Migration Database
- Model Eloquent
- Seeder Database
- Bootstrap UI
- Pencarian kategori
- Detail kategori dan anggota
