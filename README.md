<h2> Praktikum 2 CSS Dasar</h2>
<h3> NIM : 312210344 </h3>
 
1. Buka Visual Studio Code ( VSCode ) 
2. Buat file baru dengan nama lab2_css_dasar.html
3. Membuat document HMTL
4. Buatlah document seperti berikut ini 

```html 
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS Dasar</title>
</head>
<body>
    <header>
        <h1> CSS Internal dan <i> Inline CSS</i></h1>
    </header>
    <nav> 
        <a href="lab_css_dasar.html">CSS Dasar</a>
        <a href="lab_css_dasar.html">CSS External</a>
        <a href="lab_css_dasar.html">HTML Dasar</a>
    </nav>
    <!-- CSS ID selector -->
    <div id="intro">
        <h1> Hello World</h1>
        <p> Kami sedang belajar HTML dan CSS dasar, pada mata kuliah <b>Pemrograman
            Web</b> di <i>Universitas Pelita Bangsa</i>. Pelajaran pertama yang kami dapat
            adalah membuat tampilan web sederhana dalam rangka mengenal tag-tag dasar HTML
            dan CSS.
        </p>
    </div>
        <!-- Class Selector-->
             <a class="button btn-primary" href ="#intro"> Informasi Selengkapnya</a>
</body>
</html>
```
5. Selanjutnya buka pada browser
![image-6](https://github.com/twn304/labweb2/assets/115573041/3283aef9-bb21-4195-806a-ef4b1ccfd42e)


6. Mendeklarasikan CSS Internal
7. Kemudian tambah deklarasi CSS Internal seperti berikut ini.

```html  
<head>
    <title>CSS Dasar</title>
        <style> 
            body {font-family:'Open Sans', sans-serif;}
            header { min-height: 80px; border-bottom: 1px solid #77CCEF;}
            h1 {font-size: 24px; color: #0F189F; text-align: center; padding: 20px 10px;}
            h1 i {color: #6D6A6B;}
        </style>
</head>
```
8. Save , lalu buka kembali pada browser ![image-2](https://github.com/twn304/labweb2/assets/115573041/46ed8892-afb9-4ccc-8b15-d2810582ac98)

9. Menambah Inline CSS dengan menambah code 
```html
<p style = "text-align: center; color: #CCD8E4;">
``` 
10. Hasil dari menambahan code
![image-3](https://github.com/twn304/labweb2/assets/115573041/7f77c2db-6e11-4eca-8d60-33dff7bf5759)

11. Membuat CSS External

12. Tambahkan code di html seperti berikut

```html
<link rel="stylesheet" href="style.css" type="text/css"
```

13. Buatlah file baru dengan nama sytle.css kemudian deklarasi CSS seperti berikut

```css
nav {
    background: #20A759;
    color : white;
    padding: 10px;
}

nav a {
    color : white;
    text-decoration: none;
    padding: 10px 20px;
}

nav .active, nav a:hover {
    background: #0B6B3A;
}
```

14. Output ![image-4](https://github.com/twn304/labweb2/assets/115573041/a8b245b0-08db-4971-ae48-4ff4f89bfeb1)

15. Menambahkan CSS Selector 
```css
/* ID Selector */

#intro {
    background: #418fb1;
    border : 1px solid #099249;
    min-width: 100px;
    padding : 10px;
}

#intro h1 {
    text-align: left;
    border : 0 ;
    color : white;
}

/* Class Selector */
.button {
    padding: 15px 20px;
    background: #BEBCBD;
    color : white; 
    display: inline-block;
    margin: 10px;
    text-decoration: none;
}

.btn-primary {
    background: #E42A42;
}
```
16. Output ![image-5](https://github.com/twn304/labweb2/assets/115573041/394e24fe-98de-437c-88a7-e00d9784c170)


<h4>Apa perbedaan pendeklarasian CSS elemen h1 {...} dengan #intro h1 {...}? berikan penjelasannya!</h4>

<details><summary><b>Answer</b></summary> 

h1 {...} akan memengaruhi semua elemen `<h1>` di halaman web.
#intro h1 {...} akan memengaruhi hanya elemen `<h1>` yang berada di dalam elemen dengan ID "intro".
</details>

<h4>Apabila ada deklarasi CSS secara internal, lalu ditambahkan CSS eksternal dan inline CSS pada elemen yang sama. Deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya!</h4>

<details><summary><b>Answer</b></summary> 

Inline CSS memiliki prioritas tertinggi dan akan digunakan jika ada.

Internal CSS `<style>` digunakan jika tidak ada inline CSS, tetapi memiliki prioritas di atas CSS eksternal.

CSS eksternal (dari file eksternal) digunakan jika tidak ada inline atau internal CSS, dengan prioritas terendah.
</details>

<h4>Pada sebuah elemen HTML terdapat ID dan Class, apabila masing-masing selector tersebut terdapat deklarasi CSS, maka deklarasi manakah yang akan ditampilkan pada browser? Berikan penjelasan dan contohnya! ( p id="paragraf-1" class="text-paragraf" )
</h4>

<details><summary><b>Answer</b></summary> 

HTML memiliki ID dan class, maka deklarasi CSS dengan ID akan memiliki prioritas tertinggi dan akan ditampilkan oleh browser, menggantikan deklarasi dengan class atau elemen.

</details>
