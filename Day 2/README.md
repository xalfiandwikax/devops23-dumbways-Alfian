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

## Task 2: Perbedaan SH dan BASH

Shell (`sh`) dan Bash (`bash`) adalah interpreter perintah (command-line interface) yang digunakan dalam sistem Unix/Linux. Keduanya digunakan untuk menjalankan perintah-perintah di terminal, membuat skrip otomatisasi, serta mengelola sistem.


### Tabel Perbedaan SH vs BASH

| **Fitur**          | **SH (Shell)**                                 | **BASH (Bourne-Again SHell)**                                                                 |
| ------------------ | ---------------------------------------------- | --------------------------------------------------------------------------------------------- |
| **Asal**           | Shell original dari Unix (Bourne Shell - `sh`) | Diperkenalkan oleh GNU Project sebagai pengganti `sh`, dengan fitur tambahan (`bash`)         |
| **Nama Lengkap**   | Bourne Shell                                   | Bourne-Again Shell                                                                            |
| **Kompatibilitas** | Tersedia di hampir semua sistem Unix/Linux     | Kompatibel ke belakang dengan `sh`, namun lebih modern dan powerful                           |
| **Interaktivitas** | Sederhana, minim fitur interaktif              | Mendukung fitur interaktif seperti autocomplete (`Tab`), history, prompt customization        |
| **Fitur Tambahan** | Hanya mendukung fitur dasar scripting shell    | Mendukung array, arithmetic expressions, command substitution, function, brace expansion dll. |
| **Error Handling** | Terbatas                                       | Lebih baik dalam penanganan error dan debugging                                               |
| **Performance**    | Lebih ringan karena fitur minim                | Sedikit lebih berat, namun sangat powerful untuk scripting                                    |
| **Digunakan di**   | Sistem lama, embedded system, init scripts     | Hampir semua distribusi Linux modern, termasuk Ubuntu, Fedora, macOS, dll                     |
| **Ekstensi File**  | `.sh`                                          | `.sh` atau `.bash`                                                                            |
| **Portabilitas**   | Lebih portabel antar Unix system               | Kurang portabel ke sistem non-Bash (jika menggunakan fitur Bash spesifik)                     |

---

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
