---
layout: post
title: SASS dan SCSS
---
# Materi: SASS dan SCSS

## 1. Pendahuluan
**SASS (Syntactically Awesome Stylesheets)** adalah sebuah preprocessor CSS yang menambahkan fitur seperti variabel, nested rules, mixins, functions, inheritance, dan lain-lain, yang tidak tersedia dalam CSS standar.

---

## 2. Perbedaan antara SASS dan SCSS

| Fitur        | SASS              | SCSS                 |
|--------------|-------------------|----------------------|
| Ekstensi     | `.sass`           | `.scss`              |
| Gaya penulisan | Tanpa `{}` dan `;` | Menggunakan `{}` dan `;` |
| Sintaks      | Indentasi seperti Python | Mirip CSS biasa     |

---
**Contoh SASS:**
```sass
$primary-color: #333

body
  font: 100% Helvetica, sans-serif
  color: $primary-color

---

**Contoh SCSS:**
```scss
$primary-color: #333;

body {
  font: 100% Helvetica, sans-serif;
  color: $primary-color;
}
 
---

## Kesimpulan

SASS dan SCSS membantu pengembang menulis CSS dengan lebih efisien, terstruktur, dan scalable.  
SCSS sangat cocok digunakan karena sintaksnya mirip dengan CSS biasa.  
Dengan fitur seperti variabel, nesting, mixins, dan modularisasi, pengelolaan gaya dalam proyek menjadi lebih cepat dan efisien.

---
