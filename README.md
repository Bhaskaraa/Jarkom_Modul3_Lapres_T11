# Jarkom_Modul3_Lapres_T11
Repositori sebagai Laporan Resmi Soal Praktikum Modul 3 Praktikum Komunikasi Data dan Jaringan Komputer 2020.\
Disusun oleh :
```
Kelompok    :   T11
Anggota     :   I Gde Made Bhaskara Jala Dhananjaya (05311840000007)
                Robby Irvine Surya                  (05311840000023)
Departemen  :   Teknologi Informasi
```
## Soal 1
UML disetting seperti topologi pada soal : \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/uml%20template.png)

- Pertama, kita menyetting di `topologi.sh` pada puTTy untuk menambahkan beberapa UML baru dan mengatur beberapa interface seperti pada ambar di bawah : \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/topolohi.png)

- Setting juga dilakukan di `bye.sh` seperti pada gambar di bawah : \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/byw.png)

- Kemudian, router **SURABAYA** disetting pada bagian `net.ipv4.ip_forward` pada file `/etc/sysctl.conf` dan diaktifka dengan comman `sysctl -p`. \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/0.png)

- Kemdudian lakukan penyettingan terhadapt setiap uml.

**SURABAYA** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/interfaces%20sby.png)

**MALANG** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/interfaces%20mlg.png)

**TUBAN** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/interface%20tuban.png)

**MOJOKERTO** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/interface%20mojokerto.png)

**SIDOARJO, GRESIK, BANYUWANGI, MADIUN** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/interfaces%20sdj%2C%20gr%2C%20bany%2C%20madn.png)

- Terakhir, lakukan setting UML dengan command `serve networking restart`. Untuk UML Client, command dijalankan Tuban sebagai DHCP Server.

## Soal 2
Setting Router **SURABAYA** agar menjadi DHCP Relay antar DHCP Server dan Client.

- Di router, install DHCP Relay dengan command `apt-get install isc-dhcp-relay`. Lalu konfigurasi isi dari `/etc/default/isc-dhcp-relay` sebagai berikut : \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/2.png)

- `SERVERS` diisi dengan alamat IP dari DHCP Server dan `INTERFACES`diisi dengan `eth1 eth2 eth3` karena pada DHCP Relay yakni **SURABAYA** akan meneruskan DHCP request dari network interface **eth1** dan **eth2**, serta meneruskannya ke DHCP Server melalui **eth3**. Setelah itu, server direstart dengan command `service isc-dhcp-relay restart`.

==================================================================================================================================================

***SISANYA EROR, KAMI TIDAK DAPAT MENERUSKAN PENGERJAAN SOAL SHIFT*** \
![](https://github.com/Bhaskaraa/Jarkom_Modul3_Lapres_T11/blob/main/Modul3/2.png)
