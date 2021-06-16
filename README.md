# Lab11Web


# Praktikum 11: PHP Framework (Codeigniter)

Langkah-langkah Praktikum
Persiapan
Sebelum memulai menggunakan Framework Codeigniter, perlu dilakukan konfigurasi pada webserver. Beberapa ekstensi PHP perlu diaktifkan untuk kebutuhan pengembangan Codeigniter 4.

Berikut beberapa ekstensi yang perlu diaktifkan:

• php-json ekstension untuk bekerja dengan JSON;

• php-mysqlnd native driver untuk MySQL;

• php-xml ekstension untuk bekerja dengan XML;

• php-intl ekstensi untuk membuat aplikasi multibahasa;

• libcurl (opsional), jika ingin pakai Curl.

Untuk mengaktifkan ekstentsi tersebut, melalu XAMPP Control Panel, pada bagian Apache klik Config -> PHP.ini

![Screenshot (194)](https://user-images.githubusercontent.com/56498195/122149519-63309580-ce86-11eb-8c5e-9e926cefdb1d.png)


Pada bagian extention, hilangkan tanda ; (titik koma) pada ekstensi yang akan diaktifkan. Kemudian simpan kembali filenya dan restart Apache web server.


![2](https://user-images.githubusercontent.com/56498195/122149653-9f63f600-ce86-11eb-966c-ed806b9690e3.PNG)



Instalasi Codeigniter 4

Untuk melakukan instalasi Codeigniter 4 dapat dilakukan dengan dua cara, yaitu cara manual dan menggunakan composer. Pada praktikum ini kita menggunakan cara 
manual.

• Unduh Codeigniter dari website https://codeigniter.com/download

• Extrak file zip Codeigniter ke direktori htdocs/lab11_ci.

• Ubah nama direktory framework-4.x.xx menjadi ci4.

• Buka browser dengan alamat http://localhost/lab11_ci/ci4/public


![3](https://user-images.githubusercontent.com/56498195/122149793-d9cd9300-ce86-11eb-9f49-088338e1a0da.PNG)


Mengaktifkan Mode Debugging

Codeigniter 4 menyediakan fitur debugging untuk memudahkan developer untuk mengetahui pesan error apabila terjadi kesalahan dalam membuat kode program.
Secara default fitur ini belum aktif. Ketika terjadi error pada aplikasi akan ditampilkan pesan kesalahan seperti berikut


![Screenshot (195)](https://user-images.githubusercontent.com/56498195/122149899-01246000-ce87-11eb-97eb-c29bea4b3183.png)


Semua jenis error akan ditampilkan sama. Untuk memudahkan mengetahui jenis errornya, maka perlu diaktifkan mode debugging dengan mengubah nilai konfigurasi 
pada environment variable CI_ENVIRINMENT menjadi development.


![Screenshot (196)](https://user-images.githubusercontent.com/56498195/122149947-17cab700-ce87-11eb-97d9-d4959be048e5.png)


Ubah nama file env menjadi .env kemudian buka file tersebut dan ubah nilai variable CI_ENVIRINMENT menjadi development.


![8](https://user-images.githubusercontent.com/56498195/122150097-51032700-ce87-11eb-84f6-3ec5f81b4974.PNG)


Contoh error yang terjadi. Untuk mencoba error tersebut, ubah kode pada file app/Controller/Home.php hilangkan titik koma pada akhir kode


![5](https://user-images.githubusercontent.com/56498195/122150157-67a97e00-ce87-11eb-86c4-e5b4735b14a1.PNG)


Struktur Direktori
Untuk lebih memahami Framework Codeigniter 4 perlu mengetahui struktur direktori dan file yang ada. Buka pada Windows Explorer atau dari Visual Studio Code -> 
Open Folder. Terdapat beberapa direktori dan file yang perlu dipahami fungsi dan kegunaannya.

• .github folder ini kita butuhkan untuk konfigurasi repo github, seperti konfigurasi untuk build dengan github action;

• app folder ini akan berisi kode dari aplikasi yang kita kembangkan;

• public folder ini berisi file yang bisa diakses oleh publik, seperti file index.php, robots.txt, favicon.ico, ads.txt, dll;

• tests folder ini berisi kode untuk melakukan testing dengna PHPunit;


• vendor folder ini berisi library yang dibutuhkan oleh aplikasi, isinya juga termasuk kode core dari system CI.

• writable folder ini berisi file yang ditulis oleh aplikasi. Nantinya, kita bisa pakai untuk menyimpan file yang di-upload, logs, session, dll. Sedangkan file-file yang berada pada root direktori CI sebagai berikut.

• .env adalah file yang berisi variabel environment yang dibutuhkan oleh aplikasi.

• .gitignore adalah file yang berisi daftar nama file dan folder yang akan diabaikan oleh Git.

• build adalah script untuk mengubah versi codeigniter yang digunakan. Ada versi release (stabil) dan development (labil).

• composer.json adalah file JSON yang berisi informasi tentang proyek dan daftar library yang dibutuhkannya. File ini digunakan oleh Composer sebagai acuan.

• composer.lock adalah file yang berisi informasi versi dari libraray yang digunakan aplikasi.

• license.txt adalah file yang berisi penjelasan tentang lisensi Codeigniter;

• phpunit.xml.dist adalah file XML yang berisi konfigurasi untuk PHPunit.

• README.md adalah file keterangan tentang codebase CI. Ini biasanya akan dibutuhkan pada repo github atau gitlab.

• spark adalah program atau script yang berfungsi untuk menjalankan server, generate kode, dll.

![6](https://user-images.githubusercontent.com/56498195/122150363-c53dca80-ce87-11eb-9dc7-5d956fee42ff.PNG)



Router terletak pada file app/config/Routes.php


![4](https://user-images.githubusercontent.com/56498195/122150445-f3bba580-ce87-11eb-865e-62d18a0e33c4.PNG)


![9](https://user-images.githubusercontent.com/56498195/122150565-29608e80-ce88-11eb-9db4-a93c46635592.PNG)


# Pertanyaan dan Tugas

Lengkapi kode program untuk menu lainnya yang ada pada Controller Page, sehingga semua link pada navigasi header dapat menampilkan tampilan dengan layout yang 
sama.









