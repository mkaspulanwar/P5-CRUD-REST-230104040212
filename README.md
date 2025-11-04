# P5-CRUD-REST-230104040212: Membangun RESTFUL CRUD API dengan Express

Proyek ini adalah hasil dari Praktikum #5 mata kuliah **Web Service Engineering** yang berfokus pada pembangunan **RESTFUL CRUD API** sederhana menggunakan **Express.js** untuk resource produk.

---

## Tim Developer

| Peran | Nama | Profil GitHub |
| :--- | :--- | :--- |
| **Pengembang Proyek** | M. Kaspul Anwar | [![](https://img.shields.io/badge/GitHub-M.KaspulAnwar-181717?style=flat&logo=github)](https://github.com/mkaspulanwar) |
| **Dosen Pengampu** | Muhayat, M. IT | [![](https://img.shields.io/badge/GitHub-Muhayat,M.IT-181717?style=flat&logo=github)](https://github.com/muhayat-lab) |

---

## Panduan Kontribusi

Kami sangat menghargai kontribusi dari komunitas. Untuk panduan lengkap tentang cara melaporkan *bug* dan mengajukan Pull Request, silakan merujuk ke dokumen **[CONTRIBUTING.md](CONTRIBUTING.md)**.

<p align="center">
  <a href="CONTRIBUTING.md">
    <img src="https://img.shields.io/badge/Kontribusi-Lihat%20Panduan-blue?style=for-the-badge&logo=github" alt="Kontribusi">
  </a>
</p>

---

## Tujuan Praktikum

1. Menjelaskan konsep dasar RESTful API dan resource.
2. Mendesain endpoint CRUD sederhana untuk satu resource.
3. Mengimplementasikan endpoint Create (POST), Read (GET list & detail), Update (PUT), dan Delete (DELETE).
4. Menguji endpoint menggunakan Postman / Thunder Client / curl.
5. Menuliskan response JSON yang konsisten (status + data + message).
6. Memahami perbedaan status code 200, 201, 400, 404, 500.
7. Menyimpan kode ke folder proyek yang rapi sesuai konvensi kelas.
8. Mendokumentasikan hasil uji dalam bentuk evidence (screenshot / export koleksi).

---

## Peralatan dan Prasyarat

| Kategori | Alat/Prasyarat | Keterangan |
| :--- | :--- | :--- |
| **Tools** | **Node.js 18+, npm, Express.js** | Lingkungan runtime dan framework utama. |
| | **Visual Studio Code** | Editor kode. |
| | **Postman / Thunder Client** | Alat untuk pengujian API. |
| **Prasyarat** | Paham **HTTP method** | GET, POST, PUT/PATCH, DELETE. |
| | Paham **Struktur JSON** | Format pertukaran data. |
| | **Node.js + npm sudah terinstall** | Untuk menjalankan Express. |

---

## Struktur Direktori Proyek

Struktur proyek ini rapi dan terorganisir, mengikuti konvensi yang ditetapkan:

```
P5-CRUD-REST-230104040212
├── evidence
│ ├── delete.png
│ ├── get-all.png
│ ├── get-by-id.png
│ ├── post.png
│ └── put.png
├── node_modules
├── LICENSE
├── package-lock.json
├── package.json
├── README.md
└── server.js
```

---

## Cara Menjalankan Proyek

1.  Buka folder proyek ini di terminal (Pastikan Anda sudah memiliki Node.js dan npm terinstal).
2.  Instal semua dependensi yang diperlukan (Express.js):
    ```bash
    npm install
    ```
    *(Jika Anda memulai dari awal, Anda mungkin perlu `npm init -y` terlebih dahulu).*
3.  Jalankan server:
    ```bash
    node server.js
    ```
4.  Jika berhasil, akan muncul pesan: `Server running on http://localhost:3000`.

---

## Desain Endpoint (RESTful CRUD untuk `/products`)

Resource utama yang digunakan adalah `/products`. Setiap produk memiliki field minimal: `id`, `name`, `price`, dan `stock`.

| No | Endpoint | Method | Deskripsi | Request Body (JSON) | Response Sukses |
| :---: | :--- | :---: | :--- | :--- | :--- |
| **1** | `/products` | **GET** | Mengambil semua produk (List) | - | **200** + list |
| **2** | `/products/:id` | **GET** | Mengambil 1 produk berdasarkan `id` (Detail) | - | **200** + object / **404** |
| **3** | `/products` | **POST** | Menambah produk baru (Create) | `{ "name": "...", "price": 0, "stock": 0 }` | **201** + object |
| **4** | `/products/:id` | **PUT** | Memperbarui data 1 produk (Replace) | `{ "name": "...", "price": 0, "stock": 0 }` | **200** + object / **404** |
| **5** | `/products/:id` | **DELETE** | Menghapus 1 produk berdasarkan `id` | - | **200** / **204** / **404** |

---

## Panduan Pengujian API

Pengujian dilakukan menggunakan alat seperti **Postman**, **Thunder Client**, atau `curl`. Pastikan server sudah berjalan di `http://localhost:3000`.

| Operasi | Method | Endpoint | Keterangan |
| :--- | :---: | :--- | :--- |
| **Get All** | **GET** | `http://localhost:3000/products` | Ambil semua produk. |
| **Get by ID** | **GET** | `/products/1` | Ambil produk dengan ID 1. |
| **Create** | **POST** | `/products` | Tambah produk baru. |
| **Update** | **PUT** | `/products/1` | Ubah produk dengan ID 1. |
| **Delete** | **DELETE** | `/products/1` | Hapus produk dengan ID 1. |

---

## Format Respon JSON (Konsisten)

API ini menggunakan format respon yang konsisten untuk kasus sukses dan error:

### Respon Sukses (Contoh POST/Create)
```json
{
  "status": "success",
  "message": "Product created",
  "data": { 
    "id": 3,
    "name": "Pulpen Pilot Biru",
    "price": 8000,
    "stock": 60 
  }
}
```

### Respon Error (Contoh Product Not Found)
```json
{
  "status": "error",
  "message": "Product not found"
}
```

## Hasil Pengujian (Evidence)
Semua fungsionalitas CRUD telah diuji menggunakan Postman/Thunder Client, dan hasilnya didokumentasikan dalam bentuk screenshot di folder `evidence/`.
Detail Praktikum
1. Topik: Membangun RESTful CRUD API dengan `Express`.
2. Aktivitas: Membangun RESTful API menggunakan Express.js dengan fitur CRUD (Create, Read, Update, Delete) untuk resource products.
3. Dosen Pengampu: Muhayat, M.IT.
4. Durasi: 1 pertemuan x 150 menit.

## Rubrik Penilaian (Total 100)

| No | Aspek Penilaian | Bobot |
| :---: | :--- | :---: |
| 1 | Struktur project & file rapi | 15% |
| 2 | Server berjalan tanpa error | 15% |
| 3 | Endpoint CRUD berfungsi semua | 35% |
| 4 | Status code & response JSON benar | 15% |
| 5 | Evidence lengkap | 10% |
| 6 | Dokumentasi singkat | 10% |
| 7 | **Total** | **100%** |

---