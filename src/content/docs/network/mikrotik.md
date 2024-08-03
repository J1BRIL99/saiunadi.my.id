---
title: Setup Mikrotik
description: tutorial setting firewall mikrotik
---

:::tip[Konfigurasi Dasar Mikrotik]
Langkah Konfigurasi:
:::

###### ```1. Menambahkan dhcp client```
> 
> Pertama-tama tambahkan dulu ***dhcp client***nya agar ada koneksi internet, yaitu dengan cara ke menu **IP -> DHCP Client**
> 
> Lalu interfacenya diisi **ether 1**
> 
> Jika sudah pastikan di bagian status itu **Bound**, ok! gass lanjuuuutttttt brooo

###### ```2. Menambahkan IP Address```
> 
> Untuk GUI klik menu **IP > Addresses > +** , kemudian masukkan IP address untuk ke internet (public). Ether 2 ya guyss …
> 
> Jika sudah maka hasilnya akan seperti ini:
> 
> Jika sudah ora kesuwen lanjut langkah berikutnya …
> 
###### ```3. Konfigurasi DNS```
> 
> Selanjutnya kita akan mengatur DNS , DNS adalah singkatan dari Domain Name Server , yang berfungsi untuk pemetaan alamat IP menjadi sebuah nama atau sebaliknya. Sebagai contoh ketika kalian browsing , apakah kalian pernah mengetikkan IP dari server website tersebut ?? contoh ketika mengakses google , kalian pasti selalu mengetikkan www.google.com atau google.com saja kan.
> 
> Dan sebagian dari kalian mungkin tidak tahu berapa alamat IP dari google. Nah itulah fungsi dari DNS yang mengubah alamat IP menjadi sebuah nama , jadi kita akan lebih mudah mengakses Website di Internet. Untuk konfigurasi DNS di Mikrotik caranya cukup mudah , kita hanya perlu memasukkan alamat IP dari DNS Server, kita bisa menggunakan DNS dari ISP atau juga bisa menggunakan DNS google (8.8.8.8 / 8.8.4.4).
> 
> Untuk mode GUI kita klik menu **IP > DNS** lalu centang bagian Allow-remote-request.
> 
> Sekarang coba test ping ke google dari Router , jika konfigurasinya benar maka hasilnya pasti sudah bisa ping ke Google.com
> 
> Oke lanjut ke langkah selanjutnya mas brooo….
> 
###### ```4. DHCP Server```
> 
> Apa gunanya dhcp server? Yaitu untuk memberikan alamat ip secara otomatis.
> 
> Untuk GUI nya bisa ke **IP -> DHCP Server** lalu pilih **DHCP Setup** kemudian pilih interface yang terhubung ke pc/laptop.
> 
> Jika sudah gak pake nanya lanjut gass ke langkah selanjutnya.
> 
###### ```5. Konfigurasi NAT```
> 
> Sekarang router kita sudah bisa terhubung ke internet. Nah untuk membuat PC client juga bisa melakukan koneksi Internet maka dibutuhkan yang Namanya NAT atau Network Address Translation.
> 
> NAT ini berfungsi untuk menerjemahkan/menyamarkan alamat IP Lokal kita menjadi alamat IP Public kita. Coba bayangin berapa banyak jaringan lokal yang memiliki IP Private sama seperti kita , jika kita tidak translate ke IP public maka website akan susah merespons permintaan karena banyaknya alamat IP lokal yang sama. Maka dari itu NAT sangat dibutuhkan di jaringan Internet.
> 
> Untuk mode GUI kita klik menu **IP > Firewall > NAT > +**
> 
> Setelah itu masukkan isikan bagian Chain dan Out-interface , untuk Out-interface masukkan interface yang mengarah ke ISP (sumber internet).
> 
> Jangan lupa di tab ***action*** , isikan dengan action = **masquerade**
> 
> Jika belum terhubung ke internet untuk windows pergi ke ***Open Network and Sharing Center*** lalu ke ***Change Adapter Settings***. dan masuk ke ***Setting lalu ***Network***.
> 
> Disable lalu Enable bagian Local Area Connection atau Ether Network.
> 
> Oke untuk konfigurasi internetnya sudah selesai, sekian dari saya terima kasih.

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

###### NAT
```asdasd```
