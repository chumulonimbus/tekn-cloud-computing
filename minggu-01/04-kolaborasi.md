### Fork
Fork adalah membuat clone dari suatu repo di GitHub milik upstream author, diletakkan ke milik kontributor. Fork hanya dilakukan sekali saja. Pada dasarnya, proses untuk fork ini meliputi:

1. Fork repo di web GitHub.
2. Clone fork tersebut di komputer lokal.

Kontributor harus mem-fork repo upstream author sehingga di repo kontributor muncul repo tersebut. Proses forking ini dijelaskan dengan langkah-langkah berikut:

1. Login ke GitHub
2. Akses repo yang akan di-fork: https://github.com/muhraflesh/project_nuxt
3. Pada sisi kanan atas, klik Fork:

![01](images/04/image-1.png)

![02](images/04/image-2.png)

4. Pilih akan ditempatkan di account mana.
![03](images/04/image-3.png)

5. Setelah proses, repo dari upstream author sudah berada di account GitHub kita (kontributor)

![04](images/04/image-4.png)

Setelah proses tersebut, clone di komputer lokal:

![05](images/04/image-5.png)

Setelah itu, konfigurasikan repo lokal kontributor. Pada kondisi saat ini, di komputer lokal sudah terdapat repo playground-1 yang berada pada direktori dengan nama yang sama. Untuk keperluan berkontribusi, ada 2 nama repo yang harus diatur:

1. origin: menunjuk ke repo milik kontributor di GitHub, hasil dari fork.
2. upstream: menunjuk ke repo milik upstream author (repo asli) di account oldstager.

Repo origin sudah dituliskan konfigurasinya pada saat melakukan proses clone dari repo kontributor. Konfigurasi repo upstream harus dibuat.

![06](images/04/image-6.png)

Tambahkan remote upstream:

![07](images/04/image-7.png)

Hasil

![08](images/04/image-8.png)

## Mengirimkan Pull Request

### Membuat Perubahan di Repo Lokal

1. Sudah ada koordinasi secara manual tentang perubahan-perubahan yang akan dilakukan.
2. Setelah melakukan perubahan-perubahan, pastikan bahwa isi repo lokal tersinkronisasi dengan repo dari upstream author.
3. Cara melakukan sinkronisasi:

![09](images/04/image-9.png)

4. Lakukan perubahan-perubahan, setelah itu push ke origin (milik kontributor)

![10](images/04/image-10.png)

![11](images/04/image-11.png)

![12](images/04/image-12.png)

![13](images/04/image-13.png)

![14](images/04/image-14.png)

![15](images/04/image-15.png)

5. Setelah itu, buka halaman Web dari repo kontributor https://github.com/chumulonimbus/project_nuxt.git. Pada halaman tersebut akan ditampilkan isi yang kita push.

![16](images/04/image-16.png)

6. Pilih Compare and pull request, kemudian isikan deskripsi PR dan klik pada Create pull request:

![17](images/04/image-17.png)

7. Pada repo upstream author, muncul angka 1 (artinya jumlahnya 1) pada Pull requests di bagian atas.
8. Upstream author bisa menyetujui setelah melakukan review: klik pada Pull requests, akan muncul PR dengan message seperti yang ditulis oleh kontributor (Add: contributor). Klik pada PR tersebut, review kemudian klik Merge pull request diikuti dengan Confirm merge. Setelah itu, status akan berubah menjadi Merged.
9. Sinkronkan semua repo (lokal maupun GitHub kontributor)

![18](images/04/image-18.png)

![19](images/04/image-19.png)

![20](images/04/image-20.png)

![21](images/04/image-21.png)

