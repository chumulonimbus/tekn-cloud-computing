1. Update Ubuntu
    1. Login kedalam ubuntu kemudian jalankan perintah berikut<br>
    ![01](images/devstack/img1.png)
    2. setelah itu lakukan Restart<br>
    ![02](images/devstack/img2.png)
2. Menambahkan user baru
    1. Jalankan perintah berikut untuk membuat user    
    ![01](images/devstack/img3.png)
    2. Beri privileges tanpa password
    ![02](images/devstack/img4.png)
    3. Kemudian ganti user ke user yang baru saja dibuat
    ![03](images/devstack/img5.png)
3. Download Devstack
    1. Clone devstack dari github   
    ![01](images/devstack/img6.png)
    2. Buat konfigurasi dengan nama local.conf
    ![02](images/devstack/img7.png)
    3. Kemudian tambahkan commands berikut
    ![03](images/devstack/img8.png)
4. Menjalankan Openstack
    1. Jalankan perintah berikut   
    ![01](images/devstack/img9.png)
    2. Proses install akan memakan waktu kurang lebih 15-20 menit
    ![02](images/devstack/img10.png)
5. Mengakses dashboard Openstack 
    1. Copy URL pada browser   
    ![01](images/devstack/img11.png)
    2. Login dengan user demo atau admin
    ![02](images/devstack/img12.png)