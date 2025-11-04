# Panduan Kontribusi

Terima kasih atas minat Anda untuk berkontribusi pada proyek **P5-CRUD-REST-230104040212**! Kontribusi dari Anda sangat berarti untuk meningkatkan kualitas dan fungsionalitas API CRUD ini.

Panduan ini menjelaskan proses dan standar yang kami harapkan untuk kontribusi.

## Aturan Umum

1.  **Gunakan Branch:** Selalu buat *branch* baru untuk pekerjaan Anda. Jangan pernah melakukan *commit* langsung ke *branch* utama (`main` atau `master`).
2.  **Jaga Kebersihan Kode:** Tulis kode yang rapi, mudah dibaca, dan mengikuti konvensi penamaan yang sudah ada (misalnya, menggunakan *camelCase* untuk variabel JavaScript).
3.  **Uji Perubahan Anda:** Pastikan perubahan yang Anda buat tidak merusak fungsionalitas yang sudah ada. Uji semua *endpoint* yang terpengaruh.
4.  **Sertakan Dokumentasi:** Jika Anda menambahkan fungsionalitas baru atau mengubah implementasi secara signifikan, perbarui *README.md* atau tambahkan catatan yang relevan.

---

## Alur Kerja Pull Request (PR)

Ikuti langkah-langkah di bawah ini untuk mengirimkan kontribusi Anda:

### 1. Fork Repositori

* **Fork** repositori ini ke akun GitHub pribadi Anda.

### 2. Clone Repositori

* *Clone* repositori yang sudah Anda *fork* ke lingkungan lokal Anda:

  ```bash
  
  git clone [https://github.com/USERNAME_ANDA/P5-CRUD-REST-230104040212.git](https://github.com/USERNAME_ANDA/P5-CRUD-REST-230104040212.git)
  cd P5-CRUD-REST-230104040212
  
  ```
  *(Ganti `USERNAME_ANDA` dengan username GitHub Anda).*

### 3. Buat Branch Baru

* Buat *branch* baru dengan nama yang deskriptif mengenai fitur atau perbaikan yang Anda kerjakan (misalnya, `fitur/tambah-validasi-stok` atau `perbaikan/status-code-put`):

  ```bash
  
  git checkout -b nama-branch-baru
  
  ```

### 4. Lakukan Perubahan

* Lakukan perubahan dan implementasi kode Anda di *branch* tersebut.
* Lakukan pengujian lokal untuk memastikan semuanya berfungsi dengan baik.

### 5. Commit Perubahan

* Tambahkan file yang diubah:

  ```bash
  
  git add .
  
  ```
* Buat pesan *commit* yang ringkas dan deskriptif:

  ```bash
  
  git commit -m "feat: Menambahkan validasi input untuk POST /products"
  
  ```
  *(Disarankan menggunakan konvensi Conventional Commits seperti `fix:`, `feat:`, `chore:`, dll.)*

### 6. Push ke Repositori Anda

* *Push* *branch* baru Anda ke repositori GitHub pribadi Anda (yang sudah di-*fork*):

  ```bash
  
  git push origin nama-branch-baru
  
  ```

### 7. Buat Pull Request (PR)

* Buka halaman GitHub repositori Anda yang sudah di-*fork*.
* GitHub biasanya akan menampilkan tombol untuk **"Compare & Pull Request"**. Klik tombol tersebut.
* **Targetkan Branch Utama:** Pastikan Anda mengajukan PR dari *branch* Anda ke *branch* utama (`main`) di repositori asli.
* **Isi Deskripsi PR:** Tulis deskripsi yang jelas tentang:
    * Apa masalah yang diselesaikan atau fitur apa yang ditambahkan.
    * Bagaimana Anda menguji perubahan tersebut.
    * Sertakan *screenshot* (jika relevan).

### 8. Review dan Merge

* Tim pengelola akan meninjau kode Anda. Mungkin ada permintaan untuk revisi.
* Setelah disetujui, PR Anda akan digabungkan (*merge*) ke *branch* utama.

Terima kasih telah membantu!
