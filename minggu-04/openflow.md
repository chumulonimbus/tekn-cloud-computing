#### Setting Virtual Machine
1. Jalankan virtualbox kemudian buka file->import
![01](images/openflow/img1.png)
2. Kemudian konfigurasi pada network adapter 2 dengan host only
![02](images/openflow/img2.png)
3. Jalankan virtualbox image dan login menggunakan username dan password mininet
![03](images/openflow/img3.png)
4. Kemudian lakukan konfigurasi network interface
![04](images/openflow/img4.png)
5. Tampahkan port TCP 2222 ke port guest 22 untuk port forwarding
![05](images/openflow/img5.png)
6. Tes dengan menjalankan putty.exe -X -P 2222 -l localhost pada command prompt komputer local
![06](images/openflow/img6.png)
![07](images/openflow/img7.png)