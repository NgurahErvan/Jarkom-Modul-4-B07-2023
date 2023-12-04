# Jarkom-Modul-3-B07-2023
> Laporan Resmi Praktikum 3 Jaringan Komputer B07
***
## Anggota Kelompok B07
1. I Gusti Ngurah Ervan Juli Ardana (5025211205)
2. Danar Sodik Priyambodo (5025211145)

## Daftar isi
- [Topologi PKT VLSM](#topologi-pkt-vlsm)
- [Topologi GNS CIDR](#topologi-gns-cidr)
- [Rute](#rute)

- [VLSM](#vlsm)
  - [Tree](#tree)
  - [Pembagian IP](#pembagian-ip)
  - [Konfigurasi Network](#konfigurasi-network)
  - [Routing](#routing)
  - [Testing](#testing)
- [CIDR](#cidr)


## Topologi PKT VLSM
<img width="382" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/1db3d89f-dddd-4203-9629-d165b7784466">

## Topologi GNS CIDR 

## Rute
<img width="371" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/21c4ecc2-785b-4801-b132-9eb12f640fc2">

Setelah membagi semua subnet beserta jumlah ip dan netmask pada masing masing netmask, selanjutnya kami mengumpulkan subnet yang memiliki netmask yang sama untuk memudahkan dalam membuat tree

## VLSM
Variable Length Subnet Masking (VLSM) adalah sebuah metode pengalamatan IP yang memungkinkan pengguna untuk menggunakan subnet mask dengan panjang yang bervariasi untuk mengoptimalkan penggunaan alamat IP dalam jaringan. VLSM memungkinkan kita untuk membagi alamat IP secara lebih efisien dengan mengalokasikan blok alamat yang lebih besar untuk subnet yang membutuhkan lebih banyak host dan blok alamat yang lebih kecil untuk subnet yang membutuhkan lebih sedikit host.
### Tree
Setelah kami membagi semua subnet dengan jumlah ip dan netmask, selanjutnya kita dapat membangun tree dari topologi yang telah kami miliki. Berikut merupakan tree dari topologi diatas

![WSPL](https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/82de7a18-a92a-4c13-87bf-c16ab98426c4)

### Pembagian IP

Berdasarkan tree yang telah kami bentuk, selanjutnya kami dapat membagi ip kepada semua node yang ada berdasarkan subneting masing masing. berikut pembagianya:

<img width="582" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/132d573f-fa01-4017-bda6-6e7f8ed65f9a">

<img width="581" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/22b469dd-2c2f-4563-86e3-abb44062b504">

### Konfigurasi Network

Setelah kami membagi ip kepada masing masing node, kami perlu melakukan konfigurasi ip kepada masing masing Node. Caramya sebagai berikut:

#### Router

#### Client atau Server

### Routing

### Testing

## CIDR
