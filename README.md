# 🌐 **LinkGuardian Pro**

**Advanced URL & Proxy Diagnostic Scanner — Multi-Threaded, Fast, and Geo-Aware**

LinkGuardian Pro adalah aplikasi Windows yang dirancang untuk melakukan analisis URL/IP secara cepat dan mendalam, baik menggunakan direct connection maupun HTTP proxy.
Dibangun dengan arsitektur multi-thread yang ringan, aplikasi ini mampu melakukan scanning skala besar tanpa membebani CPU dan menjaga UI tetap responsif.

---

## 🚀 **Fitur Utama**

### 🔎 **1. Multi-Threaded URL Scanner**

* Melakukan pengecekan URL/IP secara paralel (hingga 20+ thread).
* UI tidak freeze dzięki penggunaan thread berbarengan.
* Scan ribuan URL dengan kecepatan tinggi.

### 🌍 **2. Mode Proxy & Non-Proxy**

* Pilih apakah ingin menggunakan HTTP Proxy (enabled/disabled).
* Auto rotate proxy berdasarkan list.
* Direct connect mode untuk pengecekan tanpa proxy.

### 📡 **3. Analisis Server Mendalam**

Untuk setiap URL yang dicek, aplikasi menampilkan:

* Status HTTP (kode + text)
* Server signature (Server Header)
* Parsed HTML Title
* Response metadata lain

### 🛰️ **4. GeoIP & ISP Lookup**

Terintegrasi dengan API GeoIP untuk pengambilan info lokasi:

* Negara
* Kota
* ISP
* Region
* Latitude/Longitude

Menggunakan IP target atau IP via proxy.

### 🧾 **5. Ekspor Otomatis (Success Only)**

Hasil sukses dapat disimpan otomatis dalam format:

* `.txt`
* `.csv`

Untuk memudahkan analisis dan dokumentasi.

### 📋 **6. Real-Time Log View**

* Hasil scan ditampilkan secara real-time.
* Auto-scroll ke item terakhir.
* Counter scan progresif (Active + Success + Failed).

### 📊 **7. Visual Progress Tracking**

* ProgressBar terintegrasi.
* Status counter: Total URL, Total Proxy, Active Scan, Result summary.

---

## 🖥️ **Teknologi yang Digunakan**

* Delphi (VCL)
* `TThread`
* `TNetHTTPClient`
* `TIdHTTP + SSL`
* Multi-threading dengan critical section
* JSON Parsing (GeoIP API)
* Regular Expressions
* ListView & Memo logger

---

## 📁 **Struktur Output**

### **CSV Output (Success Only)**

```
URL,StatusCode,StatusText,Title,Server,ISP,City,Region,Country,Lat,Lon,ProxyIP,ProxyPort
```

### **TXT Output (Success Only)**

```
[URL - StatusText] [Title - Server] [ISP - City - Region - Country - Lat - Lon] [ProxyIP:Port] - Success
```

---

## ⚙️ **Cara Penggunaan**

### **1. Siapkan file input**

* `IPs.txt` → daftar URL/IP (satu per baris)
* `Proxies.txt` → daftar proxy `IP:PORT`

### **2. Jalankan aplikasi**

Program akan memuat daftar URL & proxy otomatis saat startup.

### **3. Klik `Start`**

* Scanner mulai bekerja multi-thread.
* Log hasil akan tampil secara real-time.

### **4. Klik `Stop`** bila ingin menghentikan proses.

---

## 📦 **Fitur Tambahan**

✔ Auto rotate proxy
✔ Exception-safe thread handling
✔ SaveSuccess otomatis
✔ Thread-safe index handling
✔ UI update dengan Synchronize
✔ Mode direct tanpa proxy
✔ Auto-scroll ListView/Memo

---

## 📜 **Lisensi**

Aplikasi “LinkGuardian Pro” dapat digunakan untuk analisis jaringan, pengujian kinerja server, atau audit URL.
Pastikan penggunaan sesuai hukum dan kebijakan jaringan Anda.

---

## ⭐ **Kontribusi & Requests**

Ingin fitur baru atau optimasi tambahan?
Silakan buka **Issues** atau **Pull Request**.

---

## ❤️ **Dukungan**

Jika proyek ini membantu Anda, berikan ⭐ di GitHub!
Kontribusi baru selalu disambut.
