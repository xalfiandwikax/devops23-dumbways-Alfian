# Tugas Dumbways Day 2

### Task
1. Buat sebuah diagram sebuah jaringan komputer dengan 4 device dengan kondisi :
- IP Class C : 192.168.11.xxx
- CIDR Block : 192.168.11.0/30
2. Jelaskan perbedaan antara SH (Shell) dan BASH (Bourne-Again Shell)
3. Buat dokumentasi/kumpulan command linux yang kalian ketahui! (Command diluar materi akan diberi nilai ++)

### Answer
1.  berikut hasil rekayasa jaringan dengan CIDR Block subnet : 192.168.11.0/30
   #### Penjelasan: 
   - Pada dasarnya untuk Block IP 192.168.11.0/30 hanya ada 4 IP dan hanya ada 2 IP yang bisa dipakai oleh host diantaranya 192.162.11.1s/d.2 yang bisa dipakai, jadi bagaimana caranya untuk bisa mengakomodir 4 host?
   - Disini kita mebutuhkan router dengan 4 interface dan membuat subnet masing-masing dan masing-masing interface harus memiliki block ip untuk masing-masing host.
![topologi alfian](https://github.com/user-attachments/assets/b9701e27-3e54-4f85-85b7-061861e4d7a3)

2. Perbedaan antara Shell dan Bash secara umum adalah baris perintah yang berkembang dari shell->bash dan keduanya memliki perbedaan yang tidak telalu banyak. Untuk shell sendiri dengan skirp minimalis sedangkan untuk bash memliki skrip lebih kaya fitur, skrip shell bisa di jalankan dengan bash sedangkan skript bash belum tentu bisa dijalankan dengan skript sh
- sheel : sytax terbatas, tidak mendukung looping, sederhana
- bash : mendukung looping, mendukung aray

3. - mkdir = Make Directori membuat direktori (folder) contoh mkdir alfian
   - ls -la = Untuk melihat list di dalam direktori serta detail akses dan kepemilikan user
   - pwd = untuk melihat posisi direktori saat ini
   - rmdir = remove direktori
   - rm -rf = untuk menghapus file atau folder secara permanen
   - cd = Change direktori untuk masuk kedalam direktori
   - sudo = untuk mengubah akses menjadi admin
   - cd .. = untuk mundur 1 langkah dari folder
   - cd ~/ = untuk balik ke folder home
   - cp = untuk copy sebuah file
   - chmod = mengubah permision drwx--rwx dll / kode permision 7:read+write+execute (rwx) 6: read+write (rw-) 5: read+execute (r-x)
   - chown = mengubah kepemilikan user
   - zypper = kalau dengan ubuntu adalah apt untuk manajement paket ( sudo apt update == sudo zypper update : untuk opensuse)
   - touch = membuat file
   - mv = untuk memindahkan sebuah file atau direktori dan juga mengubah nama
   - cat = menampilkan isi file
   - nano = menampilkan texteditor bawaan linux
   - find = untuk menacari sebuah file berdasarkan nama
   - grep = mencari text di dalam file
