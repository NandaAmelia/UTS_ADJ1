- Nama   : Nanda Amelia
- Nim    : 191402015

# UTS_ADJ1
- link youtube: 
- link tutorial: https://docs.gns3.com/docs/using-gns3/advanced/connect-gns3-internet/ 

INSTALISASI, KONFIGURASI DAN MENGHUBUNGKAN GNS3 KE INTERNET(server lokal)

1.	Download GNS3 vm dari github
![1](https://user-images.githubusercontent.com/66839985/138457969-52dd6add-3528-45c1-824f-3aa4e0b52666.png)

2.  Import GNS3 VM menggunakan Virtual box
![2](https://user-images.githubusercontent.com/66839985/138457972-3293fed4-c73e-4de2-a174-299d4b3b6667.png)

3.	Masukkan file GNS3 yang telah didownload
![3](https://user-images.githubusercontent.com/66839985/138457977-091d8e9f-7271-4e9c-9e9b-4fa12d758fb5.png)
![4](https://user-images.githubusercontent.com/66839985/138457980-259427f1-977d-432e-89d2-325f5a028f11.png)
![5](https://user-images.githubusercontent.com/66839985/138457986-daaa1db8-404c-43a0-8c92-e96d8e724f60.png)
![6](https://user-images.githubusercontent.com/66839985/138458022-bed93dcf-c4bf-4ad5-8475-336121414c6f.png)

4.	Set network adapter: Host Only adapter
![7](https://user-images.githubusercontent.com/66839985/138458041-aaadde0c-6439-4075-8f33-6d33ccc61c61.png)

5.	Install GNS3 app
![8](https://user-images.githubusercontent.com/66839985/138458056-11ec147e-d7da-420d-9ac5-ca7f5833b6a6.png)
![9](https://user-images.githubusercontent.com/66839985/138458068-3104e169-0cab-4f8e-83dd-2a74205603ec.png)

6.	menggunakan setup wizard , pilih host binding : 127.0.0.1
![10](https://user-images.githubusercontent.com/66839985/138458074-34ec564b-5cfc-4a30-8006-06a7060798f5.png)
![11](https://user-images.githubusercontent.com/66839985/138458078-4e511c1b-426a-49b4-9d7c-1e31ec5cc35d.png)

7.	hubungkan kevirtual box
![12](https://user-images.githubusercontent.com/66839985/138458083-e0f4f49a-bab0-4338-8945-e0ddff9050ed.png)
![13](https://user-images.githubusercontent.com/66839985/138458092-fdc639cd-0d80-459e-ae80-404567531a31.png)

8. jika berhasil maka tampilannya akan seperti ini
![16](https://user-images.githubusercontent.com/66839985/138458096-dd20ff8a-e84f-4f64-978d-45ef2d8d76e2.png)


KONFIGURASI Open Vswitch Container
1.	Download opern Vswitch container dan Cisco 3725
![19](https://user-images.githubusercontent.com/66839985/138458102-6aaac37a-576b-4167-b178-0068b5c24ee4.png)
![20](https://user-images.githubusercontent.com/66839985/138458107-a7848bdd-0db7-4977-b449-f0abdc8d7cc8.png)
![21](https://user-images.githubusercontent.com/66839985/138458111-97403453-a0b2-4248-8690-cfe4946c97c1.png)

2. mengimport file open vswitch dan Cisco 3725/image
![22](https://user-images.githubusercontent.com/66839985/138458117-de9ac3f8-e6d0-4406-8ac1-51894e9d8d4e.png)
![23](https://user-images.githubusercontent.com/66839985/138458124-757ad8bb-8f0c-4990-b79c-6b0069f9d7f7.png)
![24](https://user-images.githubusercontent.com/66839985/138458127-47a53c65-0121-4b82-ace3-a3b89d12ae7b.png)
![25](https://user-images.githubusercontent.com/66839985/138458132-d09270b2-632b-4956-a593-59a95dd750d6.png)
![26](https://user-images.githubusercontent.com/66839985/138458134-ff90125d-51d2-4669-8f85-b4d4f5d15988.png)


MENGHUBUNGKAN GNS3 KE INTERNET(server lokal)
Langkah-langkah berikut menunjukkan cara menghubungkan instalasi GNS3 lokal ke Internet. Dalam dokumen ini topologi sederhana dari dua router Cisco digunakan untuk menunjukkan:
- Menambahkan cloud ke topologi GNS3
- Mengonfigurasi pengalamatan IP
-	Mengonfigurasi resolusi DNS
-	Mengkonfigurasi NAT pada router Cisco
-	Rute Iklan di OSPF
-	Pengujian

1.	membuat topologi GNS3 baru, pilih device toolbar dan klik people router tombol, Seret dan lepas router lokal ke GNS3 Workspace
![1 1](https://user-images.githubusercontent.com/66839985/138457886-a241d5ac-9fa4-45d7-8750-893da9c981fe.png)

2. Seret dan lepas node Cloud ke Workspace , pilih server lokal , lalu klik OK :
![1 2](https://user-images.githubusercontent.com/66839985/138457896-ab013927-bdeb-467c-b4ea-356f50752760.png)

3.	Klik tombol Perangkat Toolbar lagi untuk menciutkan grup, Klik kanan pada Cloud dan kemudian klik Configure
![1 3](https://user-images.githubusercontent.com/66839985/138457899-64250c5f-8521-4435-9a2e-f76f24752fbd.png)

4.	Daftar antarmuka Ethernet yang tersedia tercantum
![1 4](https://user-images.githubusercontent.com/66839985/138457908-76068d66-96d0-4680-8036-e841a481b35e.png)

5.	mengaktifkan "tampilkan antarmuka ethernet khusus", dan kemudian melihat daftar dropdown
![1 5](https://user-images.githubusercontent.com/66839985/138457917-e7ea9b7d-72a5-4c7a-9e76-6307533dd12d.png)

6.	Kursor mouse akan berubah untuk menunjukkan bahwa tautan dapat ditambahkan. Klik antarmuka dan kemudian pilih cloud di topologi untuk menghubungkan antarmuka ke sana. Dalam contoh ini FastEthernet 0/0 pada R1 dipilih. Selanjutnya, klik pada node Cloud, untuk melihat daftar antarmuka yang tersedia
![1 6 (2)](https://user-images.githubusercontent.com/66839985/138457921-a66e5d49-cdbd-44da-b14f-c98aef5ad4c6.png)

7. Tambahkan tautan lain antara R2 dan R1
![1 6](https://user-images.githubusercontent.com/66839985/138457927-b1cd676b-58c7-47ca-b3c9-4098fe992899.png)

8.	klik tombol Show/Hide interface labels pada GNS3 Toolbar untuk menampilkan label interface pada topologi
![1 7](https://user-images.githubusercontent.com/66839985/138457936-d21ea7c0-109e-467a-b643-f938bcf722ff.png)

9.	Sekarang siap untuk menyalakan perangkat jaringan Anda. Klik tombol Start/Resume pada GNS3 Toolbar untuk memulai perangkat jaringan 
![1 8](https://user-images.githubusercontent.com/66839985/138457940-73da8094-8e5c-46d5-9a3e-1ec350455eb0.png)
![1 9](https://user-images.githubusercontent.com/66839985/138457943-a530d47d-f052-4f90-882f-edcc442ccaa7.png)
![1 10](https://user-images.githubusercontent.com/66839985/138457947-608720a4-8096-4262-96b7-5d312ca15941.png)

10.	untuk mengonfigurasi perangkat Anda. Klik tombol Console connect to all devices pada Toolbar untuk membuka koneksi ke setiap perangkat di topologi
![1 11](https://user-images.githubusercontent.com/66839985/138457954-e2f11628-8de2-4f3f-a07c-6e8f72f381fa.png)
![1 12](https://user-images.githubusercontent.com/66839985/138457963-8a937cfa-5f25-4eee-b64e-11879d218855.png)

11.	Configurasi Ip Address.
R1# configure terminal
R1(config)# interface FastEthernet 0/0
R1(config-if)# ip address 192.168.1.123 255.255.255.0
R1(config-if)# no shutdown
R1(config-if)# exit

•	Configure a default gateway
R1(config)# ip route 0.0.0.0 0.0.0.0 192.168.1.249
R1(config)# end

•	Ping the router’s default gateway
R1# ping 192.168.1.249
![Screenshot (473)](https://user-images.githubusercontent.com/66839985/138457829-e6213d22-f813-44e5-ae0c-64c644b14249.png)
