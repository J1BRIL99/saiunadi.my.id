---
title: Konfigurasi Dasar Mikrotik
description: Tutorial konfigurasi dasar jaringan mikrotik
---

:::tip[Tutorial Dasar Networking Dalam Dunia IT]
Pengenalan fungsinya dasar Mikrotik dan winbox?
:::
>
> ###### Pengenalan fungsinya dasar Mikrotik dan winbox?
>
> ```Mikrotik``` merupakan sebuah sistem operasi berbasis perangkat lunak (software) yang digunakan untuk mengubah komputer menjadi sebuah router dalam suatu jaringan. Menggunakan sistem operasi yang berbasis Linux dan menjadi dasar bagi router jaringan.
>
> ```Winbox``` adalah salah satu aplikasi untuk konfigurasi Mikrotik RouterOS menggunakan GUI. Aplikasi Winbox bisa berjalan pada windows berbentuk portable binary, tapi bisa juga berjalan pada Linux dan MACOS (OSX) menggunakan Wine. Semua fungsi pada aplikasi Winbox hampir sama persis dengan fungsi konsol (command line).
>
###### ```1. Menambahkan DHCP client```
> 
> DHCP (Dynamic Host Configuration Protocol) berfungsi berfungsi dalam memastikan supaya perangkat yang terhubung di sebuah jaringan memperoleh alamat IP sesuai dengan yang diberikan server atau sumber internet, yaitu dengan cara ke menu:
>
> ```IP -> DHCP Client ->``` pada tab ```DHCP Client``` klik ```( + ) ->``` tab ```DHCP``` pada ```Interface``` pilih ```ether1 -> Apply/OK```
>
> ```ether1``` disini sebagai suber masuk Internet.
>
> ![lynis](/images/mikrotik/gambar1.webp "lynis")
> 
> Lihat pada menu tab ```DHCP Client``` pastikan di bagian ```Interface //> status //> Bound```
>
###### ```2. Menambahkan IP Address```
> 
> Fungsi dari IP Address yang paling utama adalah menangani koneksi antar perangkat pengirim dan penerima melalui sebuah jaringan. IP Address ini adalah sebuah alamat yang mengidentifikasi perangkat di internet.
>
> ```IP -> Addresses ->``` tab ```Address List``` klik ```( + ) ->``` bagian ```Address``` isikan ```IP ->``` bagian ```Interface``` pilih ```ether5 -> Apply/OK```
>
> ```ether5``` disini di peruntukan untuk (public) atau internet keluar.
> 
> ![lynis](/images/mikrotik/gambar2.webp "lynis")
> 
###### ```3. Konfigurasi DNS```
> 
>Konfigurasi DNS digunakan untuk menyediakan resolusi nama domain untuk router maupun perangakat klien yang terhubung dengannya atau mikrotik itu sendiri.
>
>kita hanya perlu memasukkan alamat IP dari DNS Server, atau bisa menggunakan DNS dari ISP dan juga bisa menggunakan DNS google (8.8.8.8 / 8.8.4.4).
>
> Pilih menu ```IP -> DNS ->``` pada bagian ```DNS Settings ->``` isikan DNS pada, ```Servers ->``` lalu centang bagian ```Allow-remote-request -> Apply/OK```
> 
> ![lynis](/images/mikrotik/gambar3.webp "lynis")
>
> Sekarang coba test ```ping``` ke google dari Router, jika konfigurasinya benar maka hasilnya pasti sudah bisa ```ping ke Google.com```
> 
> ![lynis](/images/mikrotik/gambar4.webp "lynis")
>
###### ```4. DHCP Server```
> 
> DHCP merupakan service yang memiliki fungsi utama mendistribusikan IP Address secara otomatis kepada setiap client yang terhubung dengan jaringan.
>
> ```IP -> DHCP Server ->``` tab ```DHCP``` klik ```( + ) ->``` menu ```DHCP Setup``` lalu ```DHCP Server Interface``` pilih= ```ether5 -> Next-Next ->``` sampai selesai kemudian ```OK```
>
> **ether5** disini sebagai sumber internet keluar (public) yang terhubung ke pc/laptop.
>
> ![lynis](/images/mikrotik/gambar5.webp "lynis")
> 
###### ```5. Konfigurasi NAT```
> 
> Network Address Translation (NAT) adalah sebuah proses pemetaan alamat IP dimana perangkat jaringan akan memberikan alamat IP Public ke perangkat jaringan local, sehingga banyak IP Private yang dapat mengakses IP Public.
>
> Pilih menu ```IP -> Firewall ->``` pada tab ```NAT ->``` klik ```( + ) ->``` tab ```General -> Chain``` isikan= ```srcnat -> Scr.Address``` isikan= ```IP Address ->``` seperti pada no.2 diatas, kemudian tab ```Action -> Action``` isikan= ```masquerade -> Apply/OK```
>
> ![lynis](/images/mikrotik/gambar6.webp "lynis")
> 
> Jika komputer belum terhubung ke internet, lakukan hal berikut:
>
> Untuk ```Windows``` pergi ke-```Open Network and Sharing Center -> Change Adapter Settings ->```
> Disable lalu Enable bagian ```Local Area Connection``` dan untuk ```Linux``` pergi ke-```Setting -> Network ->``` Disable lalu Enable pada ```Wired connection```
> 
> ![lynis](/images/mikrotik/gambar7.webp "lynis")
