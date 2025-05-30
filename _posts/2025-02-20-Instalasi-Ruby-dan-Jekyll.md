---
layout: post
title: "Panduan Instalasi Ruby dan Jekyll"
---

20 Feb 2025

---

![Panduan Instalasi Ruby dan Jekyll](/assets/image/jkil.png)

Panduan lengkap untuk menginstal Ruby, Jekyll, dan membuat personal website menggunakan GitHub Pages.

---

## 1. Instalasi

### a) **Install Ruby dan Jekyll**

1. **Cek apakah Ruby sudah terpasang**  
   Buka terminal atau Command Prompt, lalu ketik:
   ```bash
   ruby -v
   ```
   Jika Ruby sudah terpasang, versi Ruby akan ditampilkan. Jika belum, lanjutkan ke langkah berikutnya.

2. **Cek RubyGems**  
   Ketik perintah berikut untuk memastikan RubyGems sudah terpasang:
   ```bash
   gem -v
   ```

3. **Cek GCC dan Make**  
   Pastikan GCC, G++, dan Make sudah terpasang dengan mengetik:
   ```bash
   gcc -v
   g++ -v
   make -v
   ```
   Jika belum terpasang, install menggunakan **MinGW** (untuk Windows) atau package manager seperti `apt` (untuk Linux).

4. **Download Ruby Installer**
   - Kunjungi [https://rubyinstaller.org](https://rubyinstaller.org).
   - Pilih versi **Ruby 2.7.0** atau lebih tinggi.
   - Ikuti instruksi instalasi hingga selesai.

5. **Install Jekyll dan Bundler**  
   Setelah Ruby terpasang, jalankan perintah berikut untuk menginstal Jekyll dan Bundler:
   ```bash
   gem install jekyll bundler
   ```

---

### b) **Install Git**

1. **Download Git Installer**
   - Kunjungi [https://git-scm.com](https://git-scm.com).
   - Pilih installer sesuai sistem operasi Anda (contoh: **64-bit untuk Windows**).

2. **Lakukan Instalasi**
   - Ikuti instruksi instalasi hingga selesai.
   - Setelah selesai, cek instalasi Git dengan perintah:
     ```bash
     git --version
     ```

---

### c) **Install Visual Studio Code**

1. **Download VSCode Installer**
   - Kunjungi [https://code.visualstudio.com](https://code.visualstudio.com).
   - Pilih installer sesuai sistem operasi Anda.

2. **Lakukan Instalasi**
   - Ikuti instruksi instalasi hingga selesai.

---

### d) **Install Google Chrome**

1. **Download Chrome Installer**
   - Kunjungi [https://www.google.com/chrome](https://www.google.com/chrome).
   - Klik tombol **Download Chrome** dan ikuti instruksi instalasi hingga selesai.

---

## 2. Membuat Personal Website dengan Jekyll dan GitHub Pages

### 1. **Buat Akun GitHub**
- Kunjungi [https://github.com](https://github.com) dan daftar akun jika belum memiliki.

---

### 2. **Buat Repository GitHub**
- Buat repository baru dengan nama:
  ```
  username.github.io
  ```
  **Contoh**: Jika username GitHub Anda adalah `faiza`, maka repository-nya adalah:
  ```
  faiza.github.io
  ```

---

### 3. **Clone Repository ke Lokal**
Buka terminal atau Command Prompt, lalu jalankan:
```bash
git clone https://github.com/username/username.github.io.git
```
**(Ganti `username` dengan username GitHub Anda)**

---

### 4. **Inisialisasi Jekyll di Folder Repository**
Masuk ke folder repository:
```bash
cd username.github.io
```
Inisialisasi Jekyll:
```bash
bundle init
```
Perintah ini akan membuat file `Gemfile` di dalam folder proyek.

---

### 5. **Edit `Gemfile`**
Buka file `Gemfile` di VSCode, lalu tambahkan kode berikut:
```ruby
source "https://rubygems.org"

gem "jekyll"
```
Kemudian jalankan perintah:
```bash
bundle install
```

---

### 6. **Buat File `index.html`**
Buat file baru bernama `index.html` di dalam folder proyek, lalu isi dengan kode berikut:
```html
<!DOCTYPE html>
<html>
<head>
  <title>My Jekyll Site</title>
</head>
<body>
  <h1>Welcome to My Jekyll Site!</h1>
  <p>This is a sample site created with Jekyll and GitHub Pages.</p>
</body>
</html>
```

---

### 7. **Build dan Jalankan Jekyll**
Jalankan perintah berikut untuk membangun website:
```bash
jekyll build
```
Untuk menjalankan server Jekyll:
```bash
jekyll serve
```
Buka di browser:
```
http://localhost:4000
```

💡 **Tips:** Untuk melihat perubahan secara otomatis di browser, gunakan:
```bash
jekyll serve --livereload
```

---

### 8. **Edit `Gemfile.lock` untuk Platform Linux**
Jika Anda menggunakan Linux, buka file `Gemfile.lock` dan tambahkan **platform linux** pada bagian `PLATFORMS`:
```
PLATFORMS
  ruby
  x86_64-linux
```

---

### 9. **Push Repository ke GitHub**
Setelah berhasil dijalankan secara lokal, upload ke GitHub dengan perintah:
```bash
git add .
git commit -m "Initial commit"
git push origin main
```

---

### 10. **Buat GitHub Actions untuk CI/CD**
1. Di dalam repository GitHub, buat folder `.github/workflows`.
2. Buat file baru bernama `jekyll.yml` di dalam folder tersebut, lalu tambahkan kode berikut:
    ```yaml
    name: Jekyll Deploy

    on:
      push:
        branches:
          - main

    jobs:
      build-deploy:
        runs-on: ubuntu-latest
        steps:
          - name: Checkout repository
            uses: actions/checkout@v2

          - name: Setup Ruby
            uses: ruby/setup-ruby@v1
            with:
              ruby-version: '2.7'

          - name: Install dependencies
            run: bundle install

          - name: Build site
            run: JEKYLL_ENV=production bundle exec jekyll build

          - name: Deploy to GitHub Pages
            uses: peaceiris/actions-gh-pages@v3
            with:
              github_token: $
              publish_dir: ./_site
    ```
3. Commit dan push ke GitHub:
    ```bash
    git add .
    git commit -m "Add GitHub Actions for Jekyll deployment"
    git push origin main
    ```

---

## ✅ **Selesai!**

Website Anda sekarang dapat diakses di:
```
https://username.github.io
```
(Ganti `username` dengan username GitHub Anda)

---

💡 **Troubleshooting:**
- Jika terjadi error karena **port konflik**, jalankan dengan perintah berikut:
  ```bash
  jekyll serve --host 0.0.0.0 --port 4001
  ```
- Jika build gagal, pastikan Ruby dan Bundler sudah terpasang dengan benar.
- Jika GitHub Pages tidak memuat, pastikan branch