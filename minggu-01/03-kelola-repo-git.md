## Membuat Repo

1.  Klik tanda button new pada bagian awal setelah login

2.  Isikan nama, keterangan, serta lisensi. Jika dikehendaki, bisa membuat repo prvate

![01](images/03/image-1.png)

3. Kemudian Klik Create Repository di bagian bawah

## Clone Repo ke local computer

1. Untuk melakukan clone ke local computer jalankan perintah berikut

![02](images/03/image-2.png)

## Mengelola Repo

### Mengubah Isi - Push Tanpa Branching dan Merging

1. Edit File Readme

![03](images/03/image-3.png)

2. Tampilkan hasil edit

![04](images/03/image-4.png)

3. Tampilkan status perubahan

![05](images/03/image-5.png)

4. Push ke hasil perubahan ke git 

![06](images/03/image-6.png)

### Mengubah Isi dengan Branching and Merging

1. Buat branch dan buat perubahan pada file README.md

![07](images/03/image-7.png)

2. Lakukan pengecekan status

![08](images/03/image-8.png)

3. Tambahkan file yang ingin dipush ke branch baru

![09](images/03/image-9.png)

4. Push ke hasil perubahan ke branch baru 

![10](images/03/image-10.png)

5. Setelah itu, kirim pull request (PR):

![11](images/03/image-11.png)

6. Setelah membuat PR, PR tersebut bisa di-merge: 

![12](images/03/image-12.png)

7. Setelah itu, Confirm Merge, branch yang kita kirimkan tadi sudah dimasukkan ke branch main. Setelah itu, merge di komputer lokal: 

![13](images/03/image-13.png)

### Sinkronisasi
Suatu saat, bisa saja terjadi kita menggunakan komputer lain dan mengedit repo melalui repo lokal di komputer lain, setelah itu pindah ke kamputer lain lagi. Saat itu, kita perlu melakukan sinkronisasi ke kemputer lokal. Perintah untuk sinkronisasi adalah:

```
$ git pull
```
### Membatalkan Perubahan
Praktik yang baik adalah membuat *branch* pada saat kita akan melakukan perubahan-perubahan. Jika perubahan-perubahan yang kita lakukan sudah sedemikian kacaunya, maka kita bisa membuat supaya perubahan-perubahan yang kacau tersebut hilang dan kembali ke kondisi bersih seperti semula.

![14](images/03/image-14.png)
![15](images/03/image-15.png)

### Undo Commit Terakhir
Suatu saat, mungkin kita sudah terlanjur mem-push perubahan ke repo GitHub, setelah itu kita baru menyadari bahwa perubahan tersebut salah. Untuk itu, kita bisa melakukan git revert.

![16](images/03/image-16.png)
![17](images/03/image-17.png)
![18](images/03/image-18.png)

Contoh di atas adalah contoh untuk mengubah README.md dengan beberapa commit. Setelh itu, kita akan mengembalikan ke posisi terakhir sebelum commit terakhir.

![19](images/03/image-19.png)

Jika commit sudah dilakukan, tetapi belum di-push ke repo GitHub (masih berada di lokal), cara membatalkannya:

![20](images/03/image-20.png)
![21](images/03/image-21.png)

Untuk kembali ke perubahan pada saat yang sudah lama, yang perlu dilakukan adalah melakukan git revert <posisi> kemudian mengedit secara manual kemudian push ke repo.

![22](images/03/image-22.png)

Setelah itu, jika dilihat pada file, akan muncul tambahan untuk memudahkan meng-edit. File ini harus di-resolve terlebih dahulu, setelah itu baru di add dan commit:

![23](images/03/image-23.png)

Edit file tersebut, setelah itu simpan.

![24](images/03/image-24.png)

Setelah itu, lanjutkan proses revert. Saat git revert --continue isikan pesan revert.

![25](images/03/image-25.png)


