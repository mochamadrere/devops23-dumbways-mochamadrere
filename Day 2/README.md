# Basic Shell & Networking

## 1. Diagram network dengan CIDR Block 192.168.11.0/30 Kelas C
![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/diagram%20network%20cidr%20blok%2030.png?raw=true)

### Penjelasan :
- 192.168.11.0/30 bagaimana cara menghitung subnet mask nya?


  11111111.11111111.11111111.**11111100**  => 128+64+32+16+8+4 = **252**

  Jadi, karena kita menggunakan IP Kelas C, Subnet mask dari /30 adalah **255.255.255.252**


- Jumlah Subnet?

  11111111.11111111.11111111.**11111100**  => 1 = x || 0 = y  => Diketahui x = 6 dan y = 2


  2^x = 2^6 = **64**


  Jadi, jumlah subnet dari /30 adalah **64**


- Jumlah Host?


  2^y = 2^2 = **2**


  Jadi, jumlah host yang bisa digunakan adalah **2**


- Blok Subnet (_Kelipatan IP Address per subnet_) ?


  256 - (_subnet mask_) = 256 - 252 = **4**


  Jadi, angka yang dijadikan untuk subnet adalah **0,4,8,12,16, dst**


- Tabel Subnetting

  ### Subnet pertama
  | **IP Network** | **192.168.11.0** |
  | -------------- | ---------------- |
  | IP Awal | 192.168.11.1 |
  | IP Akhir | 192.168.11.2 |
  | IP Broadcast | 192.168.11.3 |

  ### Subnet kedua
  | **IP Network** | **192.168.11.4** |
  | -------------- | ---------------- |
  | IP Awal | 192.168.11.5 |
  | IP Akhir | 192.168.11.6 |
  | IP Broadcast | 192.168.11.7 |


## 2. SH(Shell) dan BASH(Bourne Again Shell)

### Definisi
Keduanya memiliki definisi yang sama yaitu program yang menyediakan Command Line Interface (CLI) yang memungkinkan user berinteraksi dengan sistem operasi atau aplikasi dengan perintah teks yang diketikan di terminal.


### Perbedaan


| SH(Shell) | BASH |
| --------- | --------- |
| Asli dari UNIX | Dibuat oleh GNU sebagai pengganti open-source untuk Bourne Shell |
| File binary biasanya ada pada /bin/sh | File binary biasanya ada pada /bin/bash |
| Fitur terbatas, karena dibuat pada era Unix lama | Lebih powerful, modern dan banyak tambahan fitur |
