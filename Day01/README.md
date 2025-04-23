# 1. Introduction to DevOps

## Apa itu DevOps ?
![alt text](https://dicoding-assets.sgp1.cdn.digitaloceanspaces.com/blog/wp-content/uploads/2020/06/apa-itu-devops.png)


DevOps merupakan singkatan dari dua kata yaitu Development dan Operations. DevOps adalah sebuah prinsip developer untuk mengkoordinasikan antar tim yaitu tim development dengan tim operations dengan efektif dan efisien.
Seperti pada gambar diatas DevOps divisualisasikan sebagai loop tak terbatas yang terdiri dari :

### Development
- Plan = Merencanakan system atau aplikasi apa yang akan diupdate.
- Code = Memastikan tim develop menjalankan tugasnya untuk fokus pada bagian coding.
- Build = Berkaitan dengan CI/CD (Continuous Integration Continuous Delivery/Deployment).
- Test = Berkaitan dengan CI/CD (Continuous Intergration Continuous Delivery/Deployment).

### Operations
- Release = Merilis system atau aplikasi ke publik.
- Deploy = Melakukan deploy ke dalam cloud computing atau server.
- Operate = dan dioperasikan dengan baik dan benar untuk menghindari server down.
- Monitor = Memonitor semua proses yang sedang berjalan.



## Tujuan DevOps
![alt text](https://dicoding-assets.sgp1.cdn.digitaloceanspaces.com/blog/wp-content/uploads/2020/06/tujuan-devops.png)

DevOps bertujuan untuk membuat seluruh proses tersebut menjadi otomatis agar:
- Mempercepat proses release ke publik.
- Menurunkan tingkat kegagalan pada rilisan terbaru.
- Mempersingkat waktu perbaikan



## Kegiatan DevOps
![alt text](https://dicoding-assets.sgp1.cdn.digitaloceanspaces.com/blog/wp-content/uploads/2020/06/DevOps-1024x580.png)

- **Continuous Integration**

  _Continuous Integration_ merupakan layanan yang diberikan DevOps untuk melakukan _build_ dan _automation testing_. Kegiatan ini dikerjakan dengan menggunakan tools berupa Source Code Repository (SCR) untuk menemukan error code dan fixed code.


- **Continuous Delivery**

  _Continuous Delivery_ selalu bekerja di dalam _software development_ untuk merubah kode. Proses ini dilakukan setelah _Continuous Integration_ untuk menambah _update_ lebih banyak untuk aplikasi yang sedang berjalan.


- **Continuous Deployment**
  
  _Continuous Deployment_ Setelah proses _Continuous Integration-Delivery_ sudah dinyatakan dengan baik, tim development dapat melihat perubahan yang terjadi pada _environment test / environment development / environment production_.


  
# 2. Virtual Machine

![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/virtual%20box.png?raw=true)

Virtual Machine yang saya gunakan adalah Orace Virtual Box.


# 3. Install Nginx WebServer ke dalam Virtual Machine

- Untuk install nginx, pertama kali kita harus mengupdate system ubuntu terlebih dahulu lalu install nginx dengan perintah sebagai berikut:

  ```sh
  sudo apt update
  ```
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/sudo%20apt%20update.png?raw=true)

  ```sh
  sudo apt install nginx
  ```
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/sudo%20apt%20install%20nginx.png?raw=true)

- Cek apakah nginx sudah terinstall dan active dengan perintah :

  ```sh
  systemctl status nginx
  ```
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/systemctl%20status%20nginx.png?raw=true)

- Lalu cek via web di windows dengan ketikan alamat ip address yang sudah kita konfigurasi sebelumnya saat penginstallan ubuntu server di virtual box :
  ![alt text](https://github.com/mochamadrere/devops23-dumbways-mochamadrere/blob/main/pict/nginx%20192.168.1.9.png?raw=true)


  # Sekian Terima Kasih
