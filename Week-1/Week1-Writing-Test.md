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