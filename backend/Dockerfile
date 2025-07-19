# backend/Dockerfile

# Gunakan base image Python
FROM python:3.11-slim

# Atur direktori kerja di dalam container
WORKDIR /app

# Salin file requirements dan instal dependensi
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Salin semua file proyek backend ke dalam container
COPY . .

# Beri tahu Docker port mana yang akan diekspos
EXPOSE 5000

# Perintah untuk menjalankan aplikasi saat container dimulai
CMD ["python", "backend.py"]