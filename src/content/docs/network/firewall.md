---
title: Sistem Firewall Pada Jaringan
description: Tutorial setting firewall mikrotik
---

:::tip[Tutorial Dasar Networking Dalam Dunia IT]
Mengenal Firewall Pada Sistem Jaringan Lokal?
:::
>
> ###### ```Firewall Pada Sistem Jaringan Lokal Menggunakan MikroTik```
>
> Firewall MikroTik adalah salah satu fitur sistem keamanan yang berfungsi untuk mengawasi dan mengontrol lalu lintas data yang masuk dan keluar dari jaringan.
>
> Tujuan konfigurasi firewall adalah untuk untuk keperluan keamanan (security), melindungi jaringan dari ancaman pihak yang tidak berwenang seperti serangan DDoS, virus, malware, akses tidak sah, dan berbagai bentuk serangan jaringan lainnya.
>
> Firewall MikroTik memiliki kemampuan yang kuat dalam mengatur dan menyaring paket data, sehingga memungkinkan sys administrator jaringan untuk memberlakukan kebijakan keamanan yang ketat.
>
> ###### ```Fungsi Firewall pada Mikrotik```
>
> Selain untuk keperluan keamanan (security), firewall mikrotik memiliki banyak fungsi lain nya yang terbagi dalam submenu pada menu ```IP –> Firewall``` di Winbox Mikrotik. Berikut penjelasan secara singkat fitur pada menu Firewall Mikrotik:
>
> ![lynis](/images/mikrotik/gambar8.webp "lynis")
> 1. ```Filter Rules```: mengijinkan (allow) atau tidak (block) paket tertentu yang melewati jaringan.
> 2. ```NAT```: melakukan port forwarding (dst nat) dan mengkoneksikan user ke jaringan internet (src nat).
> 3. ```Mangle```: menandai paket tertentu untuk diproses di fitur firewall lain seperti filter dan NAT.
> 4. ```RAW```: mem-bypass atau memblok paket tertentu sebelum masuk connection tracking yang bisa mengurangi beban CPU.
> 5. ```Connection tracking```: melihat detail koneksi yang melewati router Mikrotik.
> 6. ```Address Lists```: membuat daftar IP Address yang dapat dijadikan grup dengan nama yang sama dan bisa digunakan pada fungsi firewall lain nya.
> 7. ```Layer7 Protocols```: metode untuk mencari pola pada ICMP/TCP/UDP streams, biasanya dipakai untuk menandai website tertentu untuk diproses pada fitur firewall lain nya.
>
> Secara umum, fungsi firewall pada Mikrotik RouterOS adalah untuk membantu mengelola akses jaringan dengan lebih efisien dan aman, sehingga dapat mengelola jaringan komputer dengan lebih baik.
>
> ###### ```Implementasi Konfigurasi Firewall pada Mikrotik```
>
> Fitur firewall pada Mikrotik dapat di manfaatkan untuk berbagai macam keperluan implementasi sebagai berikut:
>
>Fitur firewall pada Mikrotik dapat di manfaatkan untuk berbagai macam keperluan implementasi sebagai berikut:
>
>Fitur firewall pada Mikrotik dapat di manfaatkan untuk berbagai macam keperluan implementasi sebagai berikut:
>
> - Memblokir port tertentu pada jaringan (Filter Rules)
> - Membuka port yang di blokir Mikrotik (Filter Rules)
> - Memblokir akses ke jaringan /IP address tertentu (Filter Rules)
> - Membuka akses ke jaringan/IP address tertentu (Filter Rules)
> - Memblokir akses ke website tertentu (Layer7 & Filter Rules)
> - Membuka akses ke website tertentu (Layer7 & Filter Rules)
> - Membuat port forwarding Mikrotik (DST NAT)
> - Membuat client bisa konek ke jaringan lain misal internet (SRC NAT)
> - Menandai koneksi yang lewat pada Mikrotik (Mangle)
> - Menandai paket yang lewat pada Mikrotik (Mangle)
> - Menandai routing yang lewat pada Mikrotik (Mangle)
> - Membuat daftar IP Address tertentu untuk dilakukan filter (Address Lists)
> - Dsb
>
> Masih banyak lagi implementasi yang bisa kita terapkan menggunakan fitur firewall Mikrotik ini. Masing-masing implementasi ini memiliki cara setting firewall Mikrotik yang berbeda-beda. Berikut contoh penerapan Konfigurasi Firewall pada Mikrotik:
>
> ```IP –> Firewall –>``` tab ```Filter Rules –>``` tambahkan rule firewall baru dengak klik tombol ```( + )``` pada tab ```General ->``` pilih ```Chain : forward``` dan ```Dst. Address``` diisi ```IP Address ->``` target yang mau di blok, misalnya IP 192.168.1.2 Kemudian masuk ke tab ```Action ->``` pada opsi Action pilih ```Drop -> Apply/OK```
>
> ![lynis](/images/mikrotik/gambar9.webp "lynis")
>
:::tip[Kesimpulan]
- Fitur Firewall pada Mikrotik memiliki fungsi yang luas, mulai dari memblokir dan mengijinkan traffic yang lewat, sampai melakukan port forwarding Mikrotik.
- Konfigurasi Firewall pada Mikrotik cukup banyak dan beragam, tergantung kebutuhan kita mau menggunakan fungsi firewall Mikrotik yang mana. Contoh penggunaan firewall Mikrotik sudah disebutkan di atas.
- Supaya setting firewall Mikrotik yang sudah di buat bisa berjalan, pastikan traffic yang melewati Mikrotik yang sudah di setting itu. Jika tidak, maka rule firewall nya tidak bisa jalan.
:::
