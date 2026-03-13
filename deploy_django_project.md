# Deploy Django Project
- Konfigurasi di dalam dokumentasi ini menggunakan VPS KVM 2 dari hostinger
- Menggunakan *'Ubuntu 24.04 LTS'*
---
## Installasi dan Persiapan
### Intallasi
- Install Python min versi ```3.xx```
### Persiapan Proyek
- Buat direktori baru pada arah ini
  ```
  cd /www/var/
  ```
  direktori baru
  ```
  mkdir projects
  ```
- Clone project menggunakan git.
- Buat Virtual Environtment baru di direktori project anda
  arah
  ```
  projects/django_project/
  ```
  venv baru
  ```
  python3 -m venv venv
  ```
  Aktifkan venv
  ```
  source venv/bin/activate
  ```
  Install Django
  ```
  pip install Django
  ```
  Install Gunicorn
  ```
  pip install gunicorn
  ```
- Konfigurasi settings.py
