# 🏅 SportsApp

Aplikasi Android yang menampilkan daftar 10 atlet dengan penghasilan tertinggi di dunia. Proyek ini dibuat sebagai sarana pembelajaran pengembangan aplikasi Android tingkat lanjut menggunakan **Kotlin**, **RecyclerView**, dan implementasi alur navigasi UX yang optimal.

![Android Studio](https://img.shields.io/badge/Android%20Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white)
![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?style=for-the-badge&logo=kotlin&logoColor=white)

---

## 🚀 Fitur Utama

* **[BARU] Halaman Beranda (Home Page):** Layar pembuka (*entry point*) sebelum masuk ke dalam katalog utama.
* **[BARU] Navigasi Kustom:** Dilengkapi tombol kembali (*back arrow*) kustom di setiap header (Katalog dan Detail) yang mempertahankan *state* aplikasi (hasil pencarian tidak reset saat kembali dari halaman detail).
* **Daftar Atlet Teratas:** Menampilkan 10 atlet dengan penghasilan tertinggi dalam format list yang modern dan responsif.
* **Fitur Pencarian (Search):** Mencari atlet secara *real-time* berdasarkan nama.
* **Halaman Detail:** Informasi mendalam tentang setiap atlet, termasuk cabang olahraga, deskripsi karier, dan total penghasilan.
* **Berbagi Informasi (Share):** Fitur Intent untuk membagikan ringkasan data atlet ke aplikasi lain (WhatsApp, Email, dll.).

---

## 🛠️ Tech Stack & Library

Aplikasi **SportsApp** dibangun menggunakan Android Native dengan bahasa **Kotlin** dan antarmuka berbasis **XML View System**. 

* **Language:** [Kotlin](https://kotlinlang.org/)
* **UI Framework:** Android XML
* **Architecture:** Master-Detail Flow dengan Custom Back Stack Management
* **Dependencies/Library:**
    * [Glide](https://github.com/bumptech/glide) - Untuk *image loading* & *caching* yang ringan.
    * **RecyclerView** - Untuk merender daftar data secara dinamis dan efisien.
    * **CardView** - Untuk memberikan efek bayangan (elevasi) dan sudut melengkung pada daftar.
    * **Serializable** - Untuk pengiriman objek data utuh antar *Activity*.

---

## 📂 Struktur Proyek

Struktur *project* disusun berdasarkan pemisahan fungsi agar mudah dipahami dan dipelihara:

```text
app
├── java/com.example.sports
│   ├── Athlete.kt             # Model data (Serializable)
│   ├── AthleteAdapter.kt      # Logic untuk RecyclerView & Search Filter
│   ├── HomeActivity.kt        # [BARU] Halaman pembuka (Beranda)
│   ├── MainActivity.kt        # Halaman katalog utama, logika Search & Navigasi
│   └── DetailActivity.kt      # Halaman detail, penerima Intent & fitur Share
├── res/layout
│   ├── activity_home.xml      # [BARU] Layout halaman beranda
│   ├── activity_main.xml      # Layout katalog dengan Custom Header & Search
│   ├── activity_detail.xml    # Layout detail atlet dengan Top Bar Navigasi
│   └── item_athlete.xml       # Layout baris untuk adapter RecyclerView
└── res/drawable               # Asset gambar atlet & UI Icons (ic_arrow_back, dll)
```
## 📸 Tampilan Aplikasi

Struktur project dan hasil tampilan aplikasi dapat dilihat pada gambar berikut.

<img width="356" height="787" alt="Screenshot 2026-04-17 172344" src="https://github.com/user-attachments/assets/23a4a32c-ee84-45df-b846-9305fcbcaec5" />

---

## 📄 Halaman Detail Atlet

Berikut tampilan halaman detail atlet saat salah satu data dipilih.

<img width="352" height="545" alt="Screenshot 2026-04-17 172358" src="https://github.com/user-attachments/assets/f27acf76-b624-429a-b2e6-207530e5aa47" />

---
