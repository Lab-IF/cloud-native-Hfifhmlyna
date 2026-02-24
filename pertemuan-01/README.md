# 📝 Laporan Praktikum - Pertemuan 1

## 🐳 Implementasi Docker Web Server (Nginx)

### 👤 Identitas
- **Nama:** Hafifa Mulyana
- **NIM:** 105841104123
- **Kelas:** 5B

---

### 🛠️ Penjelasan Tugas
Pada praktikum pertama ini, saya mempelajari dasar-dasar Docker dengan melakukan deploy sebuah web server statis menggunakan **Nginx**. Tugas ini mencakup pembuatan file HTML sederhana dan membungkusnya ke dalam Docker Container.

### 📁 Struktur File
- `index.html` : Berisi data diri/biodata singkat.
- `Dockerfile` : Instruksi untuk membangun image berbasis Nginx.
- `img/` : Folder berisi bukti screenshot hasil praktikum.

---

### 🖼️ Screenshot Hasil

#### 1. Tampilan Web Biodata (Localhost)
![Biodata](img/ss-nginx.png)
*Keterangan: Hasil running container Nginx yang menampilkan file index.html pada port 80/8080.*

#### 2. Status Docker Desktop
![Docker Status](img/ss-docker-desktop.png)
*Keterangan: Menunjukkan bahwa container untuk pertemuan 1 sedang berjalan (running) di Docker Desktop.*

---

### 📑 Langkah Kerja
1. Membuat file `index.html`.
2. Membuat `Dockerfile` dengan instruksi `FROM nginx:alpine`.
3. Melakukan build image dengan perintah: 
   `docker build -t biodata-hafifa .`
4. Menjalankan container dengan perintah: 
   `docker run -d -p 8080:80 --name web-biodata-hafifa biodata-hafifa`

---

### 💡 Kesimpulan
Dengan Docker, kita dapat menjalankan web server dengan sangat cepat tanpa harus menginstall Nginx secara manual di sistem operasi utama. Hal ini memastikan aplikasi berjalan sama di setiap komputer.
