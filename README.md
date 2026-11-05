# Mosa Studio — MVP responsive design editor

Prototype **orisinal** yang terinspirasi oleh alur kerja editor desain seperti FigCraft, bukan fork/rebranding FigCraft. Seluruh kode editor ada dalam `index.html`; tanpa framework, dependensi, akun, atau backend.

## Menjalankan

- Untuk desktop: buka `index.html` di browser terbaru (Chrome, Safari, Edge, Firefox). Editor utama tetap berjalan menggunakan `file://`.
- Untuk tablet / HP dan install sebagai web app: unggah isi folder ini ke hosting HTTPS statis (misalnya GitHub Pages / Netlify). Akses URL hosting dari perangkat. Pilih **Add to Home Screen** bila tersedia.
- Untuk uji server lokal: jalankan `python -m http.server 8000` di folder ini, lalu buka `http://localhost:8000`. Tablet/HP di jaringan yang sama bisa membuka IP LAN laptop jika firewall mengizinkan. PWA install membutuhkan HTTPS atau localhost.

## Fitur yang berjalan

- Canvas desktop, tablet, mobile, zoom, panning, gesture pinch zoom.
- Tambah rectangle, ellipse, text, button, frame, upload image (maks. 6 MB).
- Pilih layer; drag via mouse/touch; resize dari keempat sudut; edit posisi, ukuran, teks, warna, sudut, opacity.
- Duplicate, hapus, urutkan depan/belakang; undo/redo; keyboard shortcuts.
- Autosave **lokal per browser/perangkat** dengan localStorage.
- Export `.png` @2x, `.svg`, dan backup/import `.json`.
- UI desktop sidebar, tablet inspector overlay, mobile bottom navigation + bottom sheets.
- Manifest dan service worker sederhana untuk cache offline setelah pertama kali dibuka lewat HTTPS.

## Batasan MVP

- **Belum ada sinkronisasi desain lintas perangkat atau kolaborasi real-time.** Autosave berlaku pada browser tempat desain dibuat. Gunakan Export JSON dan import ke perangkat lain.
- Belum ada login, backend, project cloud, components/variants, vector pen tools, auto layout, smart prototyping, AI/MCP, atau multi-page.
- Konten teks SVG diekspor dengan font Arial; perataan teks kompleks mungkin sedikit berbeda dari preview HTML.
- PWA/offline support tergantung browser, HTTPS, dan kebijakan penyimpanan cache; `file://` tidak menjalankan service worker.
- Desain dengan gambar ukuran besar dapat melampaui kuota localStorage.

## Lisensi

Contoh kode starter ini disediakan untuk dikembangkan. FigCraft punya lisensi proyek tersendiri; contoh ini tidak menggunakan kode sumber FigCraft.
