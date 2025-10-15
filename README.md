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
```css
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
```css
.div4 {
    background-color: blue;
    clear: left;
    float: none;
}
```
## Penjelasan
Properti clear: left digunakan agar “Div 4” tampil di bawah tiga kotak sebelumnya, bukan sejajar dengan mereka.

