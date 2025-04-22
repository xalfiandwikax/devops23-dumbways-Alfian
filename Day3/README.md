### Taks
1. Akses server menggunakan terminal (Windows Terminal/PuTTY/etc.)
2. Konfigurasi ssh kalian agar bisa di akses hanya menggunakan publickey (password dimatikan)
3. Buat step by step penggunaan text manipulation! (grep, sed, cat, echo)
4. Nyalakan ufw dengan memberikan akses untuk port 22, 80, 443, 3000, 5000 dan 6969!

### Answer

1. - Pastikan kita sudah install open ssh dengan perintah ```sudo zypper in openssh-server```
   - Pastikan juga kita menjalankan dan mengaktifkan open ssh dengan perintah ```sudo systemctl enable sshd``` dan ```sudo systemctl start ssh`` untuk menjalankan open ssh, lalu periksa apakah open ssh sudah berjalan dengan perintah "sudo systemctl status sshd".
   - disaat saya mencoba akses remote menggunakan Windowspowershell ada kesalahan disebabkan belum menambahkan service firewall-cmd ketikan perintah ``` sudo firewall-cmd --add-service=ssh --permanent```
   - lalu kita berhasil akses server dengan perintah ``` ssh xalfiandwikax@192.168.99.228 ``` dan kita masukan password untuk login

![image](https://github.com/user-attachments/assets/42b9d162-a975-47c3-8ddf-45da56037ee4)
![WhatsApp Image 2025-04-22 at 23 38 43](https://github.com/user-attachments/assets/b6c87838-0024-4472-990b-36c64b1e8c7a)

2. - Konfigurasi ssh menggunakan privkey kita pastikan sudah mengenerate privkey dan pubkey di pc client dengan perintah ``` ssh-keygen ``` disini saya menyimpan key tersebut didalam direktori `` C:/User/Admin/.ssh/Alfian ```
   - Setelah berhasil generate privkey dan pubkey, Lalu kita simpan isi dari pubkey ke dalam direktori server ~/.ssh/authorized_keys menggunakan text editor bawaan linux dengan perintah ``` nano authorized_keys ``` jika belum ada file authorized_keys buat secara manual menggunakan perintah ``` touch authorized_keys ``` atau dengan ``` echo "pubkey yang sudah digenerate" > authorized_keys ``` dan pastikan berada di posisi path ``` ~/.ssh```
   - Setelah berhasil menyimpan Pubkey didalam ruanglinkum server, kita coba akses ssh kembali dengan perintah ``` ssh -i ./privatekey xalfiandwikax@192.168.99.228 ``` 
![WhatsApp Image 2025-04-23 at 01 34 33](https://github.com/user-attachments/assets/30c49048-6316-40c0-b46b-ee094f0fdac9)
     
![WhatsApp Image 2025-04-23 at 01 35 45](https://github.com/user-attachments/assets/3ebe53b5-7ef6-4ea7-a777-3027f363ea60)

![WhatsApp Image 2025-04-23 at 01 34 33 (1)](https://github.com/user-attachments/assets/a3fd102b-a879-4344-b651-e8bf70d1fc96)

3. - Membuat manipulasi text dengan cat 
* ```  cat uji1 ``` untuk menjalankan sebuah file
- ![image](https://github.com/user-attachments/assets/bed90d22-54f1-4d9c-9919-6994ab152509)
  * ``` cat uji1 uji2 >> gabungantext1 ``` menjalankan 2 file sekaligus membuat file dengan nama gabungantext1
  * ``` cat uji1 uji2 ``` menjalankan sekaligus 2 file
- ![image](https://github.com/user-attachments/assets/960b3705-0bf8-4d5c-ba52-7f993cf14481)
  - Membuat manipulasi text dengan grep
    * ``` grep "dumways" textgabung ``` mencari text didalm file dengan kata dumways
    * ``` grep -c dumways gabungtext1 ``` menghitung jumlah kata dumways pada yang berada di dalam file
- ![image](https://github.com/user-attachments/assets/a20be6f4-28c8-4e9c-b41e-6185751e70fe)
- ![image](https://github.com/user-attachments/assets/79994a2d-e413-4c0f-8f60-79cb6013a880)
 - Membuat manipulasi text dengan sed
    * ``` sed '4d' gabungtext1 ``` menghapus text baris ke 4 pada file
    *  ``` sed '2,4p' gabungtext1 ``` menampilkan text baris ke 2 dan 4 pada file  
   - ![image](https://github.com/user-attachments/assets/065db898-2b55-41e5-9a97-23aeb45e5e3f)
   - ![image](https://github.com/user-attachments/assets/4fd338d3-aa01-45d8-a77f-76788300ca5e)
  
  - Membuat manipulasi text dengan echo
     * ``` echo "alfian" > dumway1 ``` membuat file dumway1 dengan isi text alfian
     * ``` echo "pastibisa" >> dumway1 ``` menambahkan text pada file dumway1 dengan isi text alfian pastibisa
     * perhatikan jikalau tanda ```>``` kegunaan untuk menimpa isi text pada file jika nama file tidak berubah sedangkan tanda ``` >> ``` untuk menambahkan text didalam file 
  - ![image](https://github.com/user-attachments/assets/258d560d-c572-4723-b91b-6e05e1492f80)

4. Aktifkan UFW
```bash
sudo ufw allow 22
```
```bash
sudo ufw allow 80
```
```bash
sudo ufw allow 443
```
```bash
sudo ufw allow 3000
```
```bash
sudo ufw allow 5000
```
```bash
sudo ufw allow 6969
```
```bash
sudo ufw status

```sudo ufw status numbered```









