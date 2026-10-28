# Air Bersih Untuk Semua

Website Edukasi Air Bersih dan Sanitasi Layak  
Tugas UTS Mata Kuliah Pemrograman Web.



## Anggota Kelompok

|No|Nama|NIM|Tugas|
|:-:|-|:-:|-|
|1|Nyoman Bisma Krisnantara|2515091072|Membuat halaman Beranda, menyusun navbar dan hero section, serta menyiapkan CSS utama agar warna dan layout konsisten.|
|2|I Nyoman Nendra Kartika Saputra|2515091101|Membuat halaman Edukasi dan Tips \& Panduan serta menulis materi tentang air bersih, konservasi, dan sanitasi.|
|3|I Komang Putra Doxtri Apridinata|2515091134|Membuat halaman Artikel dan Tentang, menyusun konten informasi, serta menambahkan tim penyusun dan referensi.|



## Deskripsi Website

**Air Bersih Untuk Semua** adalah website edukasi yang membahas pentingnya air bersih, sanitasi layak, perlindungan sumber air, dan kebiasaan sehari-hari untuk menjaga ketersediaan air. Website ini menyajikan informasi melalui halaman edukasi, tips dan panduan, artikel, serta informasi mengenai tujuan dan tim penyusun website.

**Tujuan**

* Memberikan pemahaman mengenai pentingnya air bersih bagi kehidupan dan kesehatan.
* Menyajikan informasi tentang sumber air, pencemaran, sanitasi, dan cara menjaga kualitas air.
* Mengajak pengunjung menerapkan kebiasaan sederhana, seperti menghemat air dan tidak membuang sampah ke sumber air.
* Mendukung pemahaman terhadap SDG 6, yaitu Air Bersih dan Sanitasi Layak.

**Manfaat**

* Pengunjung memperoleh informasi dasar tentang air bersih dan sanitasi.
* Pengunjung dapat mempelajari kebiasaan untuk menghemat air dan menjaga sumber air.
* Pengunjung dapat membaca artikel edukatif dan mengenali sumber referensi terkait air bersih.

**Sasaran pengguna:** pelajar, masyarakat umum, keluarga, dan komunitas yang ingin mempelajari pentingnya air bersih.



## Halaman Website

|Halaman|File|Isi|
|-|-|-|
|Beranda|`index.html`|Halaman utama website yang memperkenalkan topik air bersih dan mengarahkan pengunjung ke konten lain.|
|Edukasi|`edukasi.html`|Informasi tentang pengertian, ciri-ciri, sumber air, dan pentingnya air bersih.|
|Tips \& Panduan|`panduan.html`|Tips dan panduan praktis untuk menghemat air serta menjaga kebersihan sumber air.|
|Artikel|`artikel.html`|Artikel edukatif tentang pentingnya air bersih, menjaga sumber air, kebiasaan menghemat air, dan peran masyarakat.|
|Tentang|`tentang.html`|Pengenalan website, tujuan dan misi, dukungan terhadap SDG 6, anggota kelompok, serta referensi.|



## Teknologi

* HTML5 untuk struktur konten setiap halaman.
* CSS3 untuk desain dan tata letak website.
* Satu berkas `css/style.css` untuk mengatur gaya bersama dan gaya khusus setiap halaman.
* Flexbox dan CSS Grid untuk tata letak elemen serta kartu konten.
* CSS Media Queries untuk menyesuaikan tampilan pada laptop, tablet, dan ponsel.
* Google Fonts (Poppins) untuk tipografi.



## Penjelasan Implementasi

### Navigasi

Semua halaman menggunakan header dan navigasi dengan lima menu: Beranda, Edukasi, Tips \& Panduan, Artikel, dan Tentang. Tautan `aria-current="page"` digunakan untuk menandai halaman yang sedang dibuka. Tampilan menu aktif dapat diatur melalui CSS tanpa harus mengubah struktur navigasi pada setiap halaman.

Contoh:

```html
<div class="menu">
    <a href="index.html">Beranda</a>
    <a href="edukasi.html">Edukasi</a>
    <a href="panduan.html">Tips \\\&amp; Panduan</a>
    <a href="artikel.html">Artikel</a>
    <a href="tentang.html" aria-current="page">Tentang</a>
</div>
```

### Layout dan gaya visual

Website menggunakan palet warna biru untuk merepresentasikan air dan lingkungan. Warna biru gelap digunakan untuk teks utama dan footer, sedangkan biru cerah digunakan sebagai aksen, tautan, serta tombol. Latar biru muda dipakai pada beberapa bagian agar pembagian konten mudah dibaca.

CSS global mengatur font, margin, padding, warna teks, navbar, tombol bersama, dan footer. Setiap halaman memiliki selector khusus—misalnya `.edukasi-hero`, `.artikel-hero`, dan `.tentang-hero`—untuk mengatur bagian yang berbeda tanpa perlu menambahkan class khusus pada elemen `<body>`.

Komponen tata letak yang digunakan antara lain:

* **Flexbox** untuk navigasi, penyelarasan konten, dan bagian yang membutuhkan pengaturan satu dimensi.
* **CSS Grid** untuk susunan gambar dan teks serta kartu edukasi, artikel, anggota kelompok, dan referensi.
* **Card** dengan border, radius, dan shadow untuk memisahkan informasi agar mudah dipindai.
* **Tombol dan tautan** untuk mengarahkan pengunjung ke halaman atau bagian terkait.

### Responsive Design

Media queries digunakan agar tata letak menyesuaikan lebar layar. Pada layar yang lebih kecil, beberapa grid berubah menjadi dua kolom atau satu kolom, jarak antarelemen dikurangi, dan gambar disesuaikan agar tidak melampaui lebar konten.

Contoh penerapan:

```css
@media (max-width: 600px) {
    .artikel-container {
        grid-template-columns: minmax(0, 1fr);
    }

    .artikel-grid {
        grid-template-columns: minmax(0, 1fr);
    }
}
```

### Gambar dan aset

Gambar ditampilkan menggunakan elemen `<img>` dengan atribut `alt` untuk memberikan deskripsi alternatif. Gambar pada kartu menggunakan `object-fit: cover` agar area gambar tetap rapi. Pastikan nama file pada atribut `src` sama persis dengan nama file yang tersimpan di folder `image/`.



## Struktur Folder

```text
air-bersih-untuk-semua/
├── index.html
├── edukasi.html
├── panduan.html
├── artikel.html
├── tentang.html
├── css/
│   └── style.css
├── image/
│   ├── logo-air.png
│   ├── river.jpg
│   ├── mata air.webp
│   ├── kebersihan air.jpg
│   ├── hemat air.jpg
│   ├── menjaga sumber air.jpeg
│   ├── sungai tentang.jpg
│   ├── foto-krisna.jpg
│   ├── foto-nendra.jpg
│   └── foto-doxtri.png
└── README.md
```

Daftar gambar di atas merupakan contoh aset yang dirujuk dalam halaman website. Pastikan susunan dan nama berkas di repository sesuai dengan folder proyek yang sebenarnya.

* `\\\*.html`: lima halaman website.
* `css/style.css`: stylesheet bersama untuk seluruh halaman.
* `image/`: gambar logo, ilustrasi, foto anggota, dan gambar pendukung konten.
* `README.md`: dokumentasi proyek.



## Website dan Repository

* **Website:** [https://bismakrisnantara-072.github.io/air-bersih/](https://bismakrisnantara-072.github.io/air-bersih/)
* **Repository:** [https://github.com/BismaKrisnantara-072/air-bersih](https://github.com/BismaKrisnantara-072/air-bersih)
Tambahkan tautan GitHub Pages dan repository pada bagian ini setelah URL proyek tersedia.



## Referensi

**Sumber materi**

* United Nations. [Sustainable Development Goal 6: Clean Water and Sanitation](https://sdgs.un.org/goals/goal6).
* World Health Organization (WHO). [Water, sanitation and hygiene (WASH)](https://www.who.int/health-topics/water-sanitation-and-hygiene-wash).
* UNICEF. [Water, Sanitation and Hygiene](https://www.unicef.org/wash).

**Aset dan tipografi**

* Google Fonts. [Poppins](https://fonts.google.com/specimen/Poppins).
* Gambar dan aset visual diambil dari pinterest

