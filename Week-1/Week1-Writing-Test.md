# **Writing & Presentation Test - Week 1**

## Unix Command Line

Dalam tampilan antarmuka kita akan mengenal 2 tampilan, yaitu GUI (Graphic User Interface) dan CLI (Command Line Interface). Pengertian singkatnya, GUI itu bisa melakukan interaksi seperti klik tombol, drag & drop, scroll dan berupa tampilan / gambar. Sedangkan CLI hanya berbasis teks saja.

### Shell

Merupakan perantara yang digunakan antara user dan sebuah sistem operasi pada komputer untuk berkomunikasi atau memerintah sistem.

### CLI (Command Line Interface)
  
CLI adalah tampilan antarmuka berbasis teks yang digunakan untuk berinteraksi dengan perangkat lunak dan sistem operasi untuk melakukan suatu tugas tertentu dengan mengetikkan perintah atau command. 

### Terminal Emulator

Adalah aplikasi atau program komputer yang digunakan untuk mengakses CLI. Dan merupakan tempat dimana shell akan berperan.

### File System Structure

Sebuah struktur untuk mengatur bagaimana data disimpan dalam sebuah sistem. Sistem operasi Windows & Unix menyusun file dan direktori menggunakan struktur yang bentuknya mirip tree seperti contoh dibawah ini :

![tree](./tree-fileSystem.png)

### Command
  
  Ada beberapa command / perintah dasar yang sering dipakai atau digunakan. Berikut contoh command / perintah berdasarkan fungsinya

  > Command untuk navigasi :
  > - Command **“pwd”** (print working directory), untuk melihat nama directory kita berada saat ini.
  > - Command **“ls”** (lists), untuk melihat isi dari directory.
  > - Command **“cd”** (change directory), untuk pindah ke directory lain.
  
  > Command untuk melihat isi file :
  > - Command **"head"**, untuk melihat beberapa line awal dari sebuah file text.
  > - Command **"tail"**, untuk melihat beberapa line akhir dari sebuah file text.
  > - Command **"cat"**, untuk melihit keseluruhan isi sebuah file.
  
  > Command untuk membuat file & directory :
  > - Command **"touch"**, untuk membuat sebuah file.
  > - Command **"mkdir"**, untuk membuat sebuah directory.
  
  > Command untuk menyalin, memindahkan, dan menghapus files & directory :
  > - Command **“cp”** (copy), untuk menyalin file, **“cp -R”** untuk menyalin directory
  > - Command **“mv”** untuk memindahkan file, **“mv -R”** untuk memindahkan directory. Bisa digunakan juga untuk mengubah nama file atau directory.
  > - Command **“rm”** (remove), untuk menghapus file, **“rm -R”** atau **“rm -d”** untuk menghapus directory


## Git & Github Dasar

### Git
Git adalah tools yang digunakan programmer. Git disini berperan sebagai Version Control System. Version Control System ini bertugas mencatat setiap perubahan pada file (termasuk code yang kita buat) pada suatu proyek baik dikerjakan secara individu maupun tim.

Jadi bisa dibilang, Git adalah aplikasi yang dapat melacak setiap perubahan yang terjadi pada suatu folder atau file. Git biasanya digunakan oleh para programmer sebagai tempat penyimpanan file pemrograman mereka karena lebih efektif dan untuk dokumentasi.

### Github
[GitHub](https://github.com/) adalah sebuah website dan layanan berbasis cloud bagi para developer untuk menyimpan dan mengelola code, serta mendokumentasikan dan mengontrol perubahannya. Selain Github, ada aplikasi lain yang bisa digunakan untuk menyimpan dan mengelola kode, serta mendokumentasikan dan mengontrol perubahannya yaitu [Gitlab](https://about.gitlab.com/) dan [BitBucket](https://lasp.colorado.edu/nucleus/login)

### Mengapa harus menggunakan Git & Github?
Dengan menggunakan GIT dan Github, kamu akan bisa bekerja dalam sebuat tim. Tujuan besarnya adalah kamu bisa berkolaborasi mengerjakan proyek yang sama tanpa harus repot copy paste folder aplikasi yang terupdate.

Kamu juga tidak perlu menunggu rekan dalam satu tim kamu menyelesaikan suatu program dahulu untuk berkolaborasi. Kamu bisa membuat file didalam projek yang sama atau membuat code di file yang sama dan menyatukannya saat sudah selesai.

### Instalasi Git
Untuk cara instalasi git sendiri sebenarnya bisa dilihat di internet karena sudah banyak yang memberikan tutorial tersebut. Atau untuk memudahkan bisa dilihat pada link berikut. [Instalasi Git](https://pendragon.netlify.app/git-installation#instalasi-git-pada-windows)

### Git Repository
Repository atau repo adalah direktory penyimpanan file proyek. Di sini, kita bisa menyimpan apa pun yang berkaitan dengan proyek yang sedang kita buat, misalnya file kode, gambar, atau audio. Repo sendiri bertempat di penyimpanan atau storage GitHub atau repositori lokal di komputer kita.

### GIT Command

- #### git config
Digunakan untuk mengatur konfigurasi tertentu sesuai keinginan pengguna, seperti email, algoritma untuk diff, username, format file, dll. Dan perintah ini cukup dijalankan sekali saja. 
Contohnya, perintah berikut bisa digunakan untuk mengatur email :
> git config --global user.email johnDoe@google.com

- #### git init
Command line dibawah akan membuat sebuah repository dan directory baru.
> git init "nama-project"

Namun, jika folder sudah ada sebelumnya. Maka kita bisa menggunakan command line berikut :
> git init .

- #### git status
Perintah ini akan menampilkan daftar file yang berubah bersama dengan file yang ingin di tambahkan atau di-commit
> git status

3 kondisi file pada git

![fileStatus](statusFile.png)

Modified adalah kondisi dimana revisi atau perubahan sudah dilakukan, tetapi belum ditandai (untracked) dan belum disimpan dalam version control.

Staged adalah kondisi dimana revisi sudah ditandai (modified) namun belum disimpan di version control.

Commit/committed adalah kondisi dimana revisi sudah disimpan pada version control.

- #### git add
Perintah git add digunakan untuk menambahkan file baru / file yang telah diubah sebelum do commit
> git add file.txt

> git add .

- #### git commit
Perintah git commit digunakan untuk melakukan commit (save) perubahan pada version control
> git commit –m “commit-message”

- #### git branch
Perintah git branch bisa digunakan untuk me-list, membuat atau menghapus branch. Untuk menampilkan semua branch yang ada di repository, gunakan:
> git branch

Untuk menghapus branch:
> git branch -d "nama-branch"

- #### git checkout
Perintah git checkout bisa digunakan untuk membuat branch atau untuk berpindah diantaranya. Misalnya, perintah berikut ini akan membuat branch baru dan berpindah ke dalamnya:
> git checkout -b "nama-branch"

Untuk berpindah dari branch satu ke lainnya, gunakan:
> git checkout "nama-branch"

- #### git remote
Perintah git remote akan membuat user terhubung ke remote repository. Perintah berikut ini akan menampilkan repository yang sedang dikonfigurasi:
> git remote -v

Perintah ini membuat user bisa menghubungkan repository lokal ke remote server:
> git remote add "alamat repository"

- #### git push
Perintah git push akan mengirimkan perubahan ke master branch dari remote repository yang berhubungan dengan directory local. Misalnya:
> git push origin master

- #### git pull
Untuk menggabungkan semua perubahan yang ada di remote repository ke directory local, gunakan perintah pull:
> git pull

- #### git merge
Perintah merge digunakan untuk menggabungkan sebuah branch ke branch aktif. Gunakan:
> git merge "nama-branch"

- #### git clone
Perintah ini digunakan jika kita ingin menduplikasi atau mendapatkan sebuah repository yang sudah ada ke dalam directory kita yang sudah terhubung dengan git.
> git clone https://github.com/libgit2/libgit2

Namun jika ingin menyimpannya ke directory lain, bisa gunakan:
> git clone https://github.com/libgit2/libgit2 mylibgit


## HTML

### Definisi
HTML adalah singkatan dari Hyper Text Markup Language. HTML adalah bahasa komputer yang digunakan untuk membuat kerangka atau struktur untuk web pages (halaman website) di internet. 

### Fungsi dan Cara kerja HTML 
Fungsi HTML adalah sebagai 'kerangka' dari sebuah website.

Web browser seperti Chrome, Firefox, Edge, Safari, atau Opera akan membaca dokumen HTML. Dokumen HTML yang berisi tag-tag HTML akan memberitahu browser bagaimana cara menampilkan sebuah konten.

### Tools Pendukung
Ada 2 tools utama yang harus dipersiapkan untuk membuat HTML, yaitu:

- Browser
- Code Editor

Browser yang direkomendasikan untuk pembuatan HTML ini adalah [Chrome](https://www.google.com/intl/id_id/chrome/). Sedangkan untuk code editor yang direkomendasikan adalah [Visual Studio Code](https://code.visualstudio.com/).

### Tag HTML
HTML terdiri dari komponen yang disebut HTML Tag. Tag adalah sebauh penanda awalan dan akhiran dari sebuah elemen di HTML. Tag dibuat dengan kurung siku (<...>), lalu di dalamnya berisi nama tag dan kadang juga ditambahkan dengan atribut.

Pada umumnya, ada 2 tipe HTML Tag:
1. **Opening Tag** (tag pembuka) - contohnya adalah `<p>`.
2. **Closing Tag** (tag penutup) - contohnya adalah `</p>`.

### Struktur Dokumen HTML
Dokumen HTML memiliki 3 tag utama, yaitu tag `<html>`, `<head>`, dan `<body>`. 

```
<!DOCTYPE html>
<html>
  <head>
    <title>Latihan</title>
  </head>
  <body>
    <h1>Hello World!</h1>
  </body>
</html>
```

- `<!DOCTYPE>` syntax mendefinisikan versi dari HTML yang digunakan dan harus dideklarasi sebelum tag `<html>`. `<!DOCTYPE html>` mendefinisikan bahwa dokumen ini adalah HTML5.
- `<html></html>` adalah root element dari halaman HTML. Semua HTML tag lainnya harus dibungkus dengan tag ini.
- `<head>` pada umumnya berisi `<meta>`, `<title>`, konten css/js internal maupun link ke file css/js eksternal.
- `<body>` berisi konten website yang ingin ditampilkan pada browser.

### HTML Element
HTML Element merupakan sebuah komponen dalam halaman web, bisa berupa paragraf, judul, atau gambar.

Struktur dari sebuah HTML element dapat digambarkan seperti ini:

![element-html](html-element.jpg)

Pada umumnya, HTML Element terdiri dari:
- **Opening Tag** (tag pembuka) - contohnya adalah `<p>`.
- **Closing Tag** (tag penutup) - contohnya adalah `</p>`.
- **Attribute** - contohnya adalah style yang memiliki Value "color=red". HTML Attribute akan kita pelajari di topik selanjutnya.
- **Content** (konten) yang ingin ditampilkan di browser - contohnya adalah My first paragraph.

Ada dua jenis HTML Element, yaitu:
1. **HTML Element** yang memiliki **Opening Tag** (tag pembuka) dan **Closing Tag** (tag penutup) - contohnya adalah `<p>` dan `</p>`.
2. **Empty HTML Element**, memiliki **Self-closing Tag**, yang hanya memiliki **Opening Tag** (tag pembuka) dengan garis miring sebelum kurung tutup - contohnya adalah `<br />` atau `<img />`.


### Tag HTML yang sering digunakan

- #### Tag Heading
Tag heading hanya memiliki 6 tingkatan. Penulisannya seperti di bawah ini:

```
<h1>Heading Satu</h1>
<h2>Heading Dua</h2>
<h3>Heading Tiga</h3>
<h4>Heading Empat</h4>
<h5>Heading Lima</h5>
<h6>Heading Enam</h6>
```

Hasilnya di browser akan seperti ini:

![html-heading](html-headings.png)

- #### Tag Paragraf
Untuk membuat paragraf pada halaman website, maka dibutuhkan tag `<p>`. Penulisannya seperti ini:

```
<p>
  Lorem ipsum dolor sit, amet consectetur adipisicing elit. Voluptate tempora
  provident quaerat officia maxime totam, repudiandae libero ducimus hic esse
  ipsam quam cum voluptates enim laudantium fugit quis eum suscipit.
</p>
```

Hasilnya di browser akan seperti ini:

![html-paragraf](html-paragraph.png)

- #### Tag Link/Anchor
Untuk membuat link pada halaman web agar bisa mengakses halaman web lain, maka diperlukan tag `<a>`. Tag `<a>` memiliki attribute href yang berguna untuk menyimpan link website yang dituju.

Penggunannya seperti ini:

```
<a href="https://youtube.com"> Youtube </a>
```

Hasilnya di browser akan seperti ini:

![link/anchor](link-anchor.png)

Dan jika kata youtube itu di klik, maka akan langsung membuka halaman website Youtube.

- #### Tag Huruf Tebal
Tag `<b>` atau `<strong>` digunakan untuk membuat tulisan menjadi tebal. Contoh penggunaannya:

```
<p>
  Nama saya <b>Sarah</b>. Saya berumur <strong>22 tahun.</strong>
</p>
```

Contoh di atas akan terlihat di browser seperti ini:

![bold-text](html-bold-text.png)

- #### Tag Huruf Miring
Untuk membuat huruf bercetak miring, maka dibutuhkan tag `<i>` atau `<em>`. Contoh penggunaan:

```
<p>
  Nama latin dari tanaman padi adalah <i>Oryza</i> <em>sativa L.</em>
</p>
```

Contoh di atas akan terlihat di browser seperti ini:

![italic-text](html-italic-text.png)

- #### Tag List
Ada dua tipe list di HTML, yaitu:

1. Unordered list dengan menggunakan tag `<ul>`
2. Ordered list dengan menggunakan tag `<ol>`

Masing-masing list baik `<ul>` atau `<ol>` memiliki element `<li>` untuk mendefinisikan nilai-nilai dari list tersebut. Contoh:

```
<!-- Unordered List -->
<ul>
  <li>Kopi</li>
  <li>Teh/li>
  <li>Susu</li>
</ul>

<!-- Ordered List -->
<ol>
  <li>Kucing</li>
  <li>Anjing</li>
  <li>Ikan</li>
</ol>
```

Contoh di atas akan terlihat di browser seperti ini:

![html-list](html-list.png)

- #### Tag Gambar
Untuk menampilkan gambar pada halaman sebuah website, maka kita membutuhkan tag `<img>`. Contoh penggunaannya:

```
<img src="https://bit.ly/3j6eb3B" alt="Cat" />
```

Hasil dari kode di atas pada browser akan terlihat seperti ini:

![html-img](html-image-tag.jpg)

- #### Tag Tabel
Pada dasarnya, untuk membuat sebuah tabel di HTML cukup membutuhkan tiga tag, yaitu:
1. `<table>` sebagai element utama.
2. `<tr>` atau dikenal sebagai table row tag, digunakan untuk membuat baris baru di dalam `<table>`.
3. `<td>` atau dikenal sebagai table data tag, digunakan sebagai container (wadah) dari data yang kita mau isi di dalam `<tr>`.

Kita juga bisa menggunakan tag `<th>` sebagai pengganti `<td>` untuk membuat header cell (biasanya digunakan untuk menampilkan judul kolom).

Secara standar `<th>` membuat tulisan di dalamnya menjadi tebal.

Cara penggunaannya seperti ini:

```
<table>
  <tr>
    <th>Nama</th>
    <th>Nomor Telpon</th>
    <th>Negara</th>
  </tr>
  <tr>
    <td>Sarah</td>
    <td>0811111111</td>
    <td>Indonesia</td>
  </tr>
  <tr>
    <td>Sophia</td>
    <td>0822222222</td>
    <td>Indonesia</td>
  </tr>
</table>
```

Pada browser, kode di atas akan terlihat seperti ini:

![table-html](html-table-example1.png)

### Deploy Project
Deploy adalah sebuah proses untuk menyebarkan atau mempublikasikan aplikasi yang sudah kita kerjakan supaya bisa digunakan oleh orang-orang. Jika aplikasi kita HTML atau Web App kita perlu mendeploy ke server. Untuk melakukan hal tersebut kita bisa menggunakan layanan yang bernama Netlify.


## CSS

### Definisi
CSS adalah singkatan dari Cascading Style Sheets. CSS adalah bahasa komputer yang digunakan untuk menambahkan design ke suatu halaman website di internet.

### Fungsi dan Cara kerja CSS
Fungsi CSS adalah sebagai 'baju' atau 'dekorator' dari sebuah website.

Apabila di dokumen HTML terdapat konten CSS maka browser akan memproses CSS tersebut dan menampilkan design sesuai dengan apa yang telah ditentukan.

### Cara menyisipkan CSS

Ada 3 cara untuk menyisipkan CSS ke dalam HTML, yaitu:
1. Inline CSS, yaitu menggunakan attribute style untuk menyisipkan kode CSS langsung di dalam HTML element.
2. Internal CSS, yaitu menggunakan element `<style>` untuk menyisipkan kode CSS. Element `<style>` tersebut diletakkan di dalam element .
3. External CSS, yaitu sebuah file CSS terpisah yang disambungkan dengan file HTML dengan menggunakan element `<link>`.

- #### Inline CSS
Inline CSS adalah cara kita memberikan attribute style kepada sebuah element dengan menyisipkannya langsung di dalam element HTML tersebut. Contoh:

```
<!DOCTYPE html>
<html>
  <head>
    <title>
      Website Pertamaku
    </title>
  </head>
  <body>
    <h1 style="color:blue;">Selamat Datang</h1>
  </body>
</html>
```

Contoh di atas akan menghasilkan teks Selamat Datang di dalam element `<h1>` berwarna biru.

![inline-css](inline-css.png)

- #### Internal CSS
Internal CSS menggunakan element `<style>` untuk menyisipkan kode CSS. Element `<style>` diletakkan di dalam element `<head>`. Contoh:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
    <style>
      body {
        background-color: yellow;
      }
      h1 {
        color: blue;
      }
      p {
        color: red;
      }
    </style>
  </head>
  <body>
    <h1>Website Pertamaku</h1>
    <p>Selamat Datang</p>
  </body>
</html>
```

Contoh di atas akan menghasilkan `<body>` dengan latar belakang berwarna kuning, tulisan di dalam `<h1>` berwarna biru, dan tulisan di dalam `<p>` berwarna merah.

![internal-css](internal-css.png)

- #### External CSS
External CSS adalah cara menyisipkan kode CSS dengan cara membuat file CSS terpisah, dan lalu menyambungkannya dengan file HTML dengan menggunakan element `<link>`. Element `<link>` tersebut diletakkan di dalam element `<head>`. 

Contoh:
Kita memiliki dua file: index.html untuk file HTML-nya dan styles.css untuk file CSS-nya.

```
<!-- File index.html -->
<!DOCTYPE html>
<html>
  <head>
    <title>Website Pertamaku</title>
    <link rel="stylesheet" href="styles.css" />
  </head>
  <body>
    <h1>Website Pertamaku</h1>
    <p>Selamat Datang</p>
  </body>
</html>
```
```
/* File styles.css */
body {
  background-color: pink;
}
h1 {
  color: blue;
}
p {
  color: black;
}
```

Contoh di atas akan menghasilkan warna `<body> `background bewarna pink, tulisan di dalam `<h1>` berwarna biru, dan tulisan di dalam `<p>` berwarna hitam.

![external-css](external-css.png)

Kelebihan lain dari menyisipkan kode CSS dengan cara external CSS adalah kita bisa menyisipkan beberapa external CSS file di halaman website kita.

Contoh:
Misalnya kita mempunyai 2 CSS file style1.css dan style2.css dan kita ingin menyisipkan kedua file ini ke dalam index.html.

### CSS Syntax
CSS Syntax adalah syntax yang digunakan untuk menunjuk atau memilih HTML element mana yang ingin diberi style (dihias). CSS syntax terdiri dari selector, property, dan value. 

Syntaxnya seperti ini:

```
selector {
  property: value;
}
```

Bisa kita gambarkan seperti vas bunga yang ingin kita hias. Kita ingin mencat vas bunga tersebut menjadi berwana merah. Yang kita cat adalah bagian tubuh (body) dari vas bunga tersebut. Jika kita kaitkan dengan CSS selector, maka:
- **Selector** adalah vas bunga, yaitu benda (HTML element, misal paragraf) mana yang akan dihias.
- **Property** adalah bagian mana dari vas bunga (dalam HTML misal, setiap huruf dari paragraf) yang akan dihias, dalam kasus ini berarti warna dari vas tersebut.
- **Value** adalah warna merah, yaitu nilai atau hiasan 'berupa apa' yang akan diberikan ke vas bunga.

### Box Model
Pada dasarnya, semua HTML element itu dianggap sebagai sebuah kotak (box). Karena hal inilah istilah box model muncul.

Box model sendiri bisa kalian anggap sebagai kotak yang membungkus setiap HTML element.

Box model terdiri dari:
- **margin** yaitu area terluar yang kosong setelah border. Margin bersifat transparan.
- **border** yaitu garis tepi yang membungkus padding dan konten.
- **padding** yaitu area kosong di antara konten dan border. Padding bersifat transparan.
- **content** yaitu konten (value/nilai) dari HTML element. Bisa berupa teks, gambar, video, ataupun suara.

Jika digambarkan, box model berbentuk seperti ini:

![box-model](box-sizing-content-box.svg)

### CSS Display
Properti Display adalah properti CSS yang paling penting untuk mengontrol tata letak. Properti Display menentukan jika/bagaimana suatu elemen ditampilkan.

Setiap elemen HTML memiliki nilai display default tergantung pada jenis elemennya. Nilai display default untuk sebagian besar elemen adalah block atau inline

Dengan properti display, kita bisa mengatur bagaimana box tersebut ditampilkan: apa box tersebut ditampilkan sebaris dengan box lain? atau satu box menempati satu baris penuh? bahkan kita juga bisa mengatur apakah box tersebut ditampilkan atau disembunyikan.

### CSS Position
Properti position menentukan jenis metode penentuan posisi yang digunakan untuk suatu element.

Ada lima nilai position yang berbeda:
1. static
2. relative
3. fixed
4. absolute
5. sticky

Element kemudian diposisikan menggunakan properti atas, bawah, kiri, dan kanan. Namun, properti ini tidak akan berfungsi kecuali properti posisi disetel terlebih dahulu. Mereka juga bekerja secara berbeda tergantung pada nilai posisi.

### Desain Website Responsif

- #### Viewport 
Secara umum viewport adalah daerah pada layar yang menampilkan suatu konten. Dalam konteks kita kali ini, tentu viewport adalah daerah yang menampilkan halaman web yang sedang kita akses.

Perlu kalian ingat bahwa ukuran viewport tidak selalu sama dengan resolusi layar perangkat.

Coba kalian cermati tangkapan layar berikut.

![viewport](viewport-mobile-desktop.svg)

Gambar di kiri merupakan tangkapan layar pada komputer; gambar di kanan pada smartphone.

Kotak berwarna hijau mewakili keseluruhan layar perangkat. Namun area yang kita sebut viewport tadi itu digambarkan oleh kotak berwarna biru.

Kembali ke permasalahan di awal: Bagaimana kita membuat halaman web kita menjadi responsif? Bagaimana kita memastikan halaman web yang kita buat nanti itu tidak terlihat buruk atau terlalu besar pada perangkat mobile?

Untuk membuat halaman website menjadi responsif, maka kita perlu menambahkan meta data berikut ini di dalam element `<head>` di file HTML.

``` 
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Meta data di atas akan mengatur viewport dari halaman website, di mana meta data tersebut akan memberikan instruksi kepada browser untuk mengatur bagaimana dimensi dan skala dari halaman website kita.
1. **width=device-width** memberitahu browser untuk mengikuti lebar layar dari perangkatnya. Sebab lebar layar tiap perangkat berbeda-beda.
2. **initial-scale=1.0** memberitahu browser tingkat pembesaran (zoom level) dari halaman itu.


- #### Media Query 
Media query merupakan modul CSS3 yang berguna membuat layout kita responsive dengan menyesuaikan tampilan berdasarkan ukuran layar perangkat. 

Terkadang tampilan yang sudah kita desain dengan sedemikian rupa bisa kacau jika ditampilkan pada tampilan mobile. Dengan media query kita dapat menyelesaikan masalah ini dengan menentukan aturan ukuran dan tata letak elemen dengan kondisi-kondisi tertentu

Media query juga disebut dengan Breakpoint, karena cara kerja media query yakni dengan cara mengecheck ukuran viewport(layar/area dimana konten terlihat) apakah sesuai dengan kondisi yang kita deklarasikan, jika benar maka kode dalam kondisi tersebut yang akan dieksekusi. Dengan kata lain media query memberikan kemampuan menggunakan kode css yang sesuai dengan kondisi yang ditentukan.

- #### Flex Box

Ada dua istilah penting saat belajar flexbox:

1. **container** adalah element yang membungkus dan mengatur tampilan dari element di dalamnya,
2. **item** adalah element dalam container yang diatur tampilannya.

Salah satu properti yang sering digunakan dalam implementasi flexbox adalah **justify-content** yang digunakan untuk mengatur tata letak dan ruang di antara item tersebut. Perhatikan kode berikut:

```
<!DOCTYPE html>
<html>

<head>
	<style>
        html, body, #flex-container {
            height: 100%;
        }
		#flex-container {
			display: flex;
			flex-direction:row;
			justify-content: flex-start;
		}
		.flex-item {
			width: 100px;
			height: 100px;
			margin: 4px;
			background: #ec5453;
			font-size: 60px;
			color: white;
			text-align: center;
		}
	</style>
</head>

<body>
	<div id="flex-container">
		<div class="flex-item">1</div>
		<div class="flex-item">2</div>
		<div class="flex-item">3</div>
	</div>
</body>

</html>
```

Ini akan menghasilkan tiga buah persegi berukuran 100px seperti ini:

![flex-start](flex-start.png)

Properti justify-content bisa diisi dengan satu dari beberapa nilai berikut:

- **flex-start** - semua item akan ditempatkan di depan seperti pada gambar di atas.
- flex-end - semua item akan ditempatkan di belakang seperti ini:
  
![flex-end](flex-end.png)

- **center** akan memampatkan semua item ke tengah:

![flex-center](flex-center.png)

- **space-between** akan memberi ruang pada setiap dua item yang bersebelahan:

![space-between](space-between.png)

- **space-around** akan memberi ruang pada sekitar tiap item:

![sapce-around](space-around.png)

