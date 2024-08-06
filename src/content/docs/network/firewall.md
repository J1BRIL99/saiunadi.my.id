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


###### Firewall
```sad a```
###### Accept/Allow
```asdasd```
###### Drop Coonection
```asdasd```
###### Scaning
```asdasd```
###### DDOS
```asdasd```
