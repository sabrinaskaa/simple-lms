Sabrina Aska Amalina - A11.2023.15264

# Simple LMS - Docker & Django

## Langkah-langkah Menjalankan Project

### 1. Clone Project

```bash
git clone https://github.com/sabrinaskaa/simple-lms.git
```

### 2. Setup Environment Variables

Copy file `.env.example` menjadi `.env` dengan:

```bash
cp .env.example .env
```

### 3. Menjalankan Docker

```bash
docker compose up --build -d
```

### 4. Cek Container

```bash
docker compose ps
```

### 5. Akses Aplikasi

Buka browser dan akses `http://localhost:8000`.

### 6. Stop Project

```bash
docker compose down
```

## Environment Variables yang Digunakan

Berikut adalah konfigurasi yang digunakan dalam file `.env`:

```bash
DEBUG=True
SECRET_KEY=django-insecure-change-this-secret-key
ALLOWED_HOSTS=localhost,127.0.0.1
DATABASE_URL=postgres://postgres:postgres@database:5432/lms_db
REDIS_URL=redis://redis:6379/0
```

Penjelasan:

- DEBUG: digunakan untuk mengaktifkan mode debug pada Django. Nilai `True` digunakan untuk development.
- SECRET_KEY: Kunci rahasia Django yang digunakan untuk keamanan aplikasi seperti session dan CSRF.
- ALLOWED_HOSTS: Daftar host yang diizinkan mengakses aplikasi.
- DATABASE_URL: Konfigurasi koneksi PostgreSQL dalam format URL dengan detail (username & password: postgres, hostname database, port PostgreSQL yaitu 5432, dan nama DB adalah lms_db)
- REDIS_URL: URL koneksi Redis

## Django Welcome Page
<img width="1920" height="1080" alt="Screenshot (23)" src="https://github.com/user-attachments/assets/323b46bd-3569-430a-aa67-9309bb9390d6" />
