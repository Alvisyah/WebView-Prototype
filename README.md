# WebView Prototype: MIT App Inventor ke React Native

Repository ini menggabungkan dua tugas mata kuliah **Pemrograman Mobile** menjadi satu alur pengembangan dengan metode **prototyping**. Aplikasi yang dikembangkan adalah aplikasi mobile sederhana yang menampilkan halaman web di dalam aplikasi menggunakan komponen **WebView**.

| Siklus | Tugas | Teknologi | Folder |
|:---:|---|---|---|
| 1 | Sesi #2: Prototype awal | MIT App Inventor | [`siklus-1-app-inventor`](siklus-1-app-inventor) |
| 2 | Sesi #3: Implementasi WebView | React Native (New Architecture / Fabric) + `react-native-webview` | [`siklus-2-react-native`](siklus-2-react-native) |

## Metode Pengembangan: Prototyping

Prototyping adalah metode pengembangan perangkat lunak yang membangun model awal (prototype) dengan cepat, mengevaluasinya, lalu memperbaikinya pada siklus berikutnya. Pada proyek ini ada dua siklus:

```
Siklus 1                                   Siklus 2
Kebutuhan -> Prototype (App Inventor)      Perbaikan kebutuhan -> Implementasi (React Native)
          -> Evaluasi ------------------>             -> Evaluasi akhir
```

## Siklus 1: Prototype Awal (MIT App Inventor)

**Tujuan:** membuat prototype aplikasi WebView dengan cepat untuk memastikan ide dasarnya berjalan, yaitu menampilkan halaman web di dalam aplikasi mobile.

**Cara membuat:** prototype dirancang secara visual di [MIT App Inventor](https://appinventor.mit.edu) menggunakan komponen `WebViewer` dan pemrograman berbasis blok, tanpa menulis kode.

**Hasil:** aplikasi dapat memuat halaman web di dalam aplikasi.

**Catatan proyek:** keterangan prototype ini ada di folder [`siklus-1-app-inventor`](siklus-1-app-inventor).

### Evaluasi Siklus 1

Prototype berhasil membuktikan konsep dan cepat dibuat, tetapi ada keterbatasan yang menjadi bahan perbaikan:

- Pengembangan berbasis blok dan komponen bawaan sehingga kontrol terhadap kode dan perilaku aplikasi terbatas.
- Sulit menambahkan pustaka pihak ketiga atau fitur kustom.
- Proyek tidak bisa dikelola dengan alur kerja pengembang pada umumnya (editor kode, Git, dependensi lewat npm).
- Tampilan dan struktur aplikasi bergantung pada kemampuan komponen yang disediakan platform.

## Siklus 2: Implementasi dengan React Native

**Tujuan:** memperbaiki prototype dengan membangun ulang aplikasi memakai kode, sehingga lebih fleksibel dan dapat dikembangkan lebih lanjut.

**Perbaikan dari siklus 1:**

- Dibangun dengan **React Native** menggunakan **New Architecture (Fabric)**.
- WebView memakai paket [`react-native-webview`](https://github.com/react-native-webview/react-native-webview).
- Kode dikelola dalam proyek terstruktur (TypeScript) dan dapat diunggah ke Git.
- Memanfaatkan komponen standar React Native (`View`, `Text`, `Image`) untuk tata letak.
- Dijalankan dan diuji pada emulator Android (Android Studio).

**Hasil:** aplikasi menampilkan halaman web (Wikipedia) di dalam WebView pada emulator Android.

### Cara Menjalankan Siklus 2

**Prasyarat:** Node.js, JDK, Android Studio beserta emulator Android (atau perangkat Android dengan USB debugging), mengikuti [panduan lingkungan React Native](https://reactnative.dev/docs/set-up-your-environment).

```bash
# 1. Kloning repository
git clone https://github.com/Alvisyah/WebView-Prototype.git
cd WebView-Prototype/siklus-2-react-native

# 2. Instal dependensi
npm install

# 3. Jalankan Metro bundler (terminal pertama)
npm start

# 4. Jalankan aplikasi di Android (terminal kedua)
npm run android
```

### Evaluasi Siklus 2

- Aplikasi berhasil berjalan dengan arsitektur modern React Native dan menampilkan halaman web melalui WebView.
- Kode lebih mudah diperluas, misalnya menambah navigasi, tombol kembali, atau indikator loading.
- Pengaturan lingkungan pengembangan lebih berat dibanding App Inventor (Node.js, Android Studio, emulator).
- Pengembangan selanjutnya dapat menambah fitur dan menyiapkan versi iOS.

## Perbandingan Kedua Siklus

| Aspek | Siklus 1 (App Inventor) | Siklus 2 (React Native) |
|---|---|---|
| Cara membangun | Blok visual, tanpa kode | Kode TypeScript/JavaScript |
| Kecepatan membuat prototype | Sangat cepat | Lebih lama, perlu setup |
| Fleksibilitas | Terbatas pada komponen bawaan | Tinggi, bisa memakai pustaka pihak ketiga |
| Pengelolaan versi | Proyek di platform App Inventor | Git, `package.json` |
| Cocok untuk | Prototype awal dan validasi ide | Pengembangan lanjutan |

## Struktur Repository

```
WebView-Prototype/
├── README.md
├── siklus-1-app-inventor/
│   └── README.md          # Keterangan prototype siklus 1
└── siklus-2-react-native/
    ├── App.tsx            # Komponen utama aplikasi
    ├── package.json
    ├── android/
    └── ios/
```

## Pengembang

**Alvisyah Hatta**
GitHub: [@Alvisyah](https://github.com/Alvisyah)
Tugas Sesi #2 dan Sesi #3, mata kuliah Pemrograman Mobile.