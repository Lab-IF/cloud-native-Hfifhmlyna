# 📝 Laporan Praktikum - Pertemuan 2

## 📦 Docker Images & Dockerfile

---

## 👤 Identitas Mahasiswa

| Field | Isi |
|-------|-----|
| **Nama** | `[Hafifa Mulyana]` |
| **NIM** | `[105841104123]` |
| **Kelas** | `[5B]` |
| **Tanggal Praktikum** | `[DD/MM/YYYY]` |

---

## 📋 Hasil Praktikum

### ✅ Checklist Tugas

| No | Tugas | Status |
|----|-------|--------|
| 1 | Buat file `app.py` | ⬜ Belum / ✅ Sudah |
| 2 | Buat file `Dockerfile` | ⬜ Belum / ✅ Sudah |
| 3 | Build image berhasil | ⬜ Belum / ✅ Sudah |
| 4 | Run container berhasil | ⬜ Belum / ✅ Sudah |
| 5 | Screenshot semua hasil | ⬜ Belum / ✅ Sudah |

---

## 💻 Kode Program

### 📄 app.py
```python
# from flask import Flask

app = Flask(__name__)

# Endpoint / (Halaman Utama)
@app.route('/')
def index():
    return '''
    <h1>Instruksi Penggunaan:</h1>
    <p>Tambahkan <b>/hello/Hafifa Mulyana</b> pada URL di browser.</p>
    <p>Contoh: <a href="/hello/Hafifa">localhost:5000/hello/Hafifa</a></p>
    '''

# Endpoint /hello/<nama> (Sesuai Hint Tugas)
@app.route('/hello/<nama>')
def hello(nama):
    return f'<h1>Halo, {nama}!</h1>'

if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=5000)


```

### 🐳 Dockerfile
```dockerfile
FROM python:3.11-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY app.py .
EXPOSE 5000
CMD ["python", "app.py"]

```

---

## 🖼️ Screenshot Hasil

> **📁 Simpan screenshot di folder:** `pertemuan-02/ss/`

### 1️⃣ Screenshot Struktur Folder Project
![Struktur Folder](ss/01-struktur-folder.png)

**Penjelasan:**
```
<img width="978" height="800" alt="image" src="https://github.com/user-attachments/assets/39aa01fc-407e-4fbd-87de-41cfa9abf083" />

```

---

### 2️⃣ Screenshot Docker Build
![Docker Build](ss/02-docker-build.png)

**Perintah yang dijalankan:**
```bash
[Tulis perintah yang dijalankan]
```

**Penjelasan:**
```
[Tulis penjelasan]
```

---

### 3️⃣ Screenshot Docker Images
![Docker Images](ss/03-docker-images.png)

**Penjelasan:**
```
[Tulis penjelasan - image apa saja yang muncul?]
```

---

### 4️⃣ Screenshot Docker Run (Output Aplikasi)
![Docker Run](ss/04-docker-run.png)

**Perintah yang dijalankan:**
```bash
[Tulis perintah yang dijalankan]
```

**Output:**
```
[Paste output yang muncul]
```

---

## 📝 Catatan & Kendala

### Kendala yang Dihadapi:
```
[Tulis kendala yang dialami selama praktikum]
```

### Solusi:
```
[Tulis solusi dari kendala tersebut]
```

---

## 💡 Kesimpulan

```
[Tulis kesimpulan yang didapat dari praktikum ini]
Contoh:
- Dockerfile adalah blueprint untuk membuat image
- Setiap instruksi di Dockerfile membuat layer baru
- dll
```

---

## 📊 Penilaian

> *Diisi oleh Dosen/Asisten*

| Kriteria | Nilai |
|----------|-------|
| Kode app.py benar | /20 |
| Dockerfile benar | /30 |
| Build berhasil | /20 |
| Screenshot lengkap | /20 |
| Kesimpulan | /10 |
| **Total** | **/100** |

**Catatan Penilai:**
```

```

---

<div align="center">

📅 **Pertemuan 2** | [🏠 Kembali ke README](README.md)

</div>
