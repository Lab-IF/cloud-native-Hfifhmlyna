# 📝 Laporan Praktikum - Pertemuan 2

## 🐍 Web Service Dinamis dengan Python Flask & Docker

### 👤 Identitas
- **Nama:** Hafifa Mulyana
- **NIM:** 105841104123
- **Kelas:** 5B

---

### 🛠️ Penjelasan Tugas
Pada pertemuan ini, saya membangun aplikasi web menggunakan **Flask** yang mendukung **Dynamic Routing**. Berbeda dengan Pertemuan 1 yang bersifat statis, aplikasi ini dapat memproses input dari URL dan menampilkannya kembali ke layar.

### 🎯 Endpoint yang Dibuat
1. `GET /` : Halaman utama yang berisi instruksi penggunaan aplikasi.
2. `GET /hello/<nama>` : Endpoint dinamis yang akan menyapa user berdasarkan nama yang diketikkan di URL.

---

### 🖼️ Screenshot Hasil

#### 1. Endpoint Greeting (/hello/Hafifa)
![Hasil Greeting](img/ss-greeting.png)
*Keterangan: Berhasil menampilkan output "Halo, Hafifa!" saat mengakses endpoint /hello/Hafifa.*

#### 2. Log Container Docker
![Docker Log](img/ss-docker-log.png)
*Keterangan: Status container tugas2-flask berjalan normal pada port 5000.*

---

### 📑 Langkah Kerja
1. **Coding**: Membuat `app.py` menggunakan framework Flask dengan logika f-string untuk greeting.
2. **Environment**: Membuat `requirements.txt` untuk dependensi Flask.
3. **Containerization**: Membuat `Dockerfile` menggunakan base image `python:3.9-slim`.
4. **Execution**: 
   - `docker build -t flask-hafifa .`
   - `docker run -d -p 5000:5000 --name tugas2-flask flask-hafifa`

---

### 💡 Kesimpulan
Praktikum ini menunjukkan kemudahan Docker dalam membungkus aplikasi berbasis bahasa pemrograman tertentu (Python). Dynamic routing pada Flask memungkinkan pembuatan aplikasi yang lebih interaktif.
