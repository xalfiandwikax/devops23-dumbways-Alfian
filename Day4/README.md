# 1. Penjelasan tentang Git

**Git** adalah sistem **version control terdistribusi**  untuk melacak perubahan kode sumber selama pengembangan software
## Konsep Dasar Git

1. **Repository (Repo)**  
   - Direktori proyek yang dilacak Git.  
   - Terdiri dari:  
     - **Repo Lokal** (di komputer developer)  
     - **Repo Remote** (contoh: GitHub/GitLab)  

2. **Commit**  
   - Snapshot perubahan dengan:  
     - ID unik (hash)  
     - Pesan commit (*commit message*)  

3. **Branch**  
   - Cabang independen kode sumber.  
   - Contoh:  
     - `main`/`master` (branch utama) 
     - `developer` (branch untuk para developer)   
     - `feature/login` (branch pengembangan fitur)  

4. **Merge**  
   - Menggabungkan perubahan antar branch.  

5. **Staging Area**  
   - Area persiapan sebelum commit (`git add .`). 

# 2. Buat sebuah repository bernama "dumbways-batch-23" yang berisi 3 file

<img src="image/pull_request_git.jpeg" alt="Contoh Commit" width="300"/>
