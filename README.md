#  Praktikum 4 - CSS Layout

##  Tujuan
Pada praktikum ini, mahasiswa diharapkan mampu:
1. Memahami struktur dasar pembuatan layout website.  
2. Mengenal dan menerapkan konsep **Box Element** dalam HTML dan CSS.  
3. Menggunakan **CSS Float Property** untuk mengatur posisi elemen.  
4. Memahami **HTML5 Semantic Element** dalam membangun struktur halaman.  
5. Membuat **layout web sederhana** menggunakan kombinasi HTML dan CSS.

---

##  Langkah-langkah Praktikum

### 1️⃣ Persiapan Awal
- Buka **VS Code** atau text editor lain.  
- Buat folder baru bernama **Lab4Web**.  
- Buat file HTML baru bernama `lab4_box.html`.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Box Element</title>
</head>
<body>
    <header>
        <h1>Box Element</h1>
    </header>
</body>
</html>
```
## Penjelasan
Langkah ini membuat struktur HTML dasar yang akan digunakan untuk percobaan Box Element.

### 2️⃣ Membuat Box Element

Tambahkan elemen div di dalam <section> untuk membuat beberapa box.
```html
<section>
    <div class="div1">Div 1</div>
    <div class="div2">Div 2</div>
    <div class="div3">Div 3</div>       
</section>
```
## Tambahkan code css di bagian <head>:
```html
<style>
    div {
        float: left;
        padding: 10px;
    }
    .div1 { background: red; }
    .div2 { background: yellow; }
    .div3 { background: green; }
</style>
```
## Penjelasan
Kode di atas membuat tiga kotak sejajar menggunakan CSS float. Setiap kotak diberi warna berbeda agar terlihat jelas.

### 3️⃣ Mengatur Clearfix Element
Tambahkan elemen tambahan untuk melihat efek dari properti clear.
```html
<div class="div4">Div 4</div>
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
```
## Penjelasan
Properti clear: left digunakan agar “Div 4” tampil di bawah tiga kotak sebelumnya, bukan sejajar dengan mereka.

### 4️⃣ Membuat Layout Sederhana

Buat folder baru bernama lab4_layout, lalu buat dua file:
## 1.home.html
## 2.style.css
Isi file home.html sebagai berikut:
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Layout Sederhana</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div id="container">
        <header><h1>Layout Sederhana</h1></header>
        <nav>
            <a href="home.html" class="active">Home</a>
            <a href="artikel.html">Artikel</a>
            <a href="about.html">About</a>
            <a href="kontak.html">Kontak</a>
        </nav>
        <section id="hero"></section>
        <section id="wrapper">
            <section id="main"></section>
            <aside id="sidebar"></aside>
        </section>
        <footer>
            <p>&copy; 2021 - Universitas Pelita Bangsa</p>
        </footer>
    </div>
</body>
</html>
```
## Penjelasan
Struktur ini menggunakan HTML5 Semantic Elements seperti <header>, <nav>, <section>, <aside>, dan <footer> untuk membuat layout yang lebih terstruktur.

### 5️⃣ Styling Layout
Tambahkan ke file style.css:
```css
/* Reset */
* { margin: 0; padding: 0; }

body {
    font-family: 'Open Sans', sans-serif;
    color: #5a5a5a;
}

#container {
    width: 980px;
    margin: 0 auto;
    box-shadow: 0 0 1em #ccc;
}

/* Header */
header { padding: 20px; }
header h1 { color: #b5b5b5; }

/* Navigasi */
nav {
    display: block;
    background-color: #1f5faa;
}
nav a {
    padding: 15px 30px;
    display: inline-block;
    color: #fff;
    text-decoration: none;
}
nav a.active, nav a:hover {
    background-color: #2b83ea;
}
```
## Penjelasan
Bagian ini mengatur tampilan halaman agar memiliki warna, jarak, dan bayangan yang rapi.

