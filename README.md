# Jarkom-Modul-4-B07-2023
> Laporan Resmi Praktikum 4 Jaringan Komputer B07
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

- Pertama, Pilihlah Router yang akan dikonfigurasi kemudian klik pada router tersebut. kami akan contohkan pada router aura

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/b0971552-94fd-45f3-9daa-e6d83f0576a9">

- Kedua, Klik config setelah itu kalian akan diberikan beberapa pilihan via mulai dari fastethernet0/0 hingga fastethernet1/1. Setelah itu kalian hanya perlu melakukan konfigurasi berdasarkan pembagian ip yang telah ada diatas

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/2fc3353c-b0c9-4fc4-b681-021cf1ebfedb">
 
- Selanjutnya, kita hanya perlu memasukan IPv4Address dan Subnet Mask berdasarkan pembagian subnetting masing masing. Contohnya Sebagai berikut:

##### Aura dan Fririen (A8) :

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/4dd3532e-665c-4ab8-9477-532b1035a6e1">

##### Aura dan Denken (A9) :

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/aeb4cfbc-3261-4085-985a-0a6283b7f0f8">

##### Aura dan Eisen (A11) :

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/d0d37d96-ee08-42ad-8f2f-169a6d91739c">

- Lakukanlah langkah yang sama pada setiap Router yang ada
  
#### Client atau Server

- Pertama, Pilihlah Client/Server yang akan dikonfigurasi kemudian klik pada Client/Server tersebut. kami akan contohkan pada Client Lakekorridor

<img width="958" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/e4907acb-a579-43c9-a516-bd07e49d76a5">

- Kedua, Klik dekstop untuk mencari pilihan ip configuration

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/b62a1f9b-aec8-444f-92ca-6a9e596c9fd9">

- Ketiga, Klik ipconfiguration. setelah itu kalian akan diminta untuk mengisi IPv4Address dan Subnet Mask. Setelah itu kalian hanya perlu melakukan konfigurasi berdasarkan pembagian ip yang telah ada diatas. Contohnya pada client Lakekorridor yang berhubungan dengan Router Frieren dengan subnet A2. Berikut konfigutasinya

<img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/7374c7f7-dc22-43ce-a39f-f7905714a924">

- Lakukanlah langkah yang sama pada setiap Client/Server yang ada
  
### Routing
Static Routing mengharuskan administrator jaringan untuk menambahkan/ memberitahukan rute (route) baru ke dalam tabel routing ketika terdapat subnet tambahan dalam jaringannya. Konsep static routing sederhana, daftarkan NID dan netmask yang ada serta tentukan gateway untuk menuju ke subnet tersebut. Caranya sebagai berikut

- Klik, setiap Route yang ingin dilakukan Routing. Kami contohkan menggunakan Router Aura
  
 <img width="959" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/fb1404e2-861a-47ea-8d35-3523b19a6710">

- Setalah itu, Pada menu Config, terdapat pilihan Routing, kemudian klik Static untuk menambahkan route pada Router yang terdiri dari Network, Mask, dan Next Hop
  
  <img width="960" alt="image" src="https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/7c880aa7-dd0e-4dba-bc1b-c361c5d4677a">

- Kemudian Isi satu persatu route, kemudian klik "Add" hingga seluruh route dari router tersebut ditambahkan. kami akan mencontohkan menggunakan Router Aura
  - Kiri
    #### A7 via Frieren
    ```
    Network : 10.12.24.64
    Mask : 255.255.255.224
    Next Hop : 10.12.24.126
    ```
    #### A4 via Frieren
    ```
    Network : 10.12.24.116
    Mask : 255.255.255.252
    Next Hop : 10.12.24.126
    ```
    #### A2 via Frieren
    ```
    Network : 10.12.24.112
    Mask : 255.255.255.252
    Next Hop : 10.12.24.126
    ```
    #### A1 via Frieren
    ```
    Network : 10.12.0.0
    Mask : 255.255.248.0
    Next Hop : 10.12.24.126
    ```
    #### A3 via Frieren
    ```
    Network : 10.12.8.0
    Mask : 255.255.252.0
    Next Hop : 10.12.24.126
    ```
    #### A5 via Frieren
    ```
    Network : 10.12.24.120
    Mask : 255.255.255.252
    Next Hop : 10.12.24.126
    ```
    #### A6 via Frieren
    ```
    Network : 10.12.24.96
    Mask : 255.255.255.248
    Next Hop : 10.12.24.126
    ```
  - Kanan
    #### A10 via Denken
    ```
    Network : 10.12.22.0
    Mask : 255.255.255.0
    Next Hop : 10.12.24.130
    ```
  - Bawah
    #### A12 via Eisen
    ```
    Network : 10.12.28.136
    Mask : 255.255.255.252
    Next Hop : 10.12.28.134
    ```
    #### A13 via Eisen
    ```
    Network : 10.12.24.104
    Mask : 255.255.255.248
    Next Hop : 10.12.28.134
    ```
    #### A14 via Eisen
    ```
    Network : 10.12.28.140
    Mask : 255.255.255.252
    Next Hop : 10.12.28.134
    ```
    #### A15 via Eisen
    ```
    Network : 10.12.12.0
    Mask : 255.255.252.0
    Next Hop : 10.12.28.134
    ```
    #### A16 via Eisen
    ```
    Network : 10.12.23.0
    Mask : 255.255.255.0
    Next Hop : 10.12.28.134
    ```
    #### A17 via Eisen
    ```
    Network : 10.12.24.144
    Mask : 255.255.255.252
    Next Hop : 10.12.28.134
    ```
    #### A18 via Eisen
    ```
    Network : 10.12.20.0
    Mask : 255.255.254.0
    Next Hop : 10.12.28.134
    ```
    #### A19 via Eisen
    ```
    Network : 10.12.24.148
    Mask : 255.255.255.252
    Next Hop : 10.12.28.134
    ```
    #### A20 via Eisen
    ```
    Network : 10.12.24.0
    Mask : 255.255.255.192
    Next Hop : 10.12.28.134
    ```
    #### A21 via Eisen
    ```
    Network : 10.12.16.0
    Mask : 255.255.252.0
    Next Hop : 10.12.28.134
    ```
- Lakukanlah langkah yang sama pada setiap router yang kalian miliki
  
### Testing

https://github.com/NgurahErvan/Jarkom-Modul-4-B07-2023/assets/114007640/c325ac4d-4feb-422c-98ba-ed4e2f0da27b

## CIDR
