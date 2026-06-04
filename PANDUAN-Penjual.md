# BlokBuild Pro — Panduan untuk Penjual

Aplikasi HTML Builder lengkap. Satu file, jalan di browser mana saja, tanpa internet (kecuali fitur opsional).

## Cara pakai (untuk pembeli)
1. Buka `BlokBuild-Pro.html` di browser (Chrome/Edge/Firefox).
2. Masukkan kunci lisensi (demo: `DEMO-2026`).
3. Pakai **✨ AI Generate** (ketik ide) atau **📑 Template** untuk mulai cepat, atau tarik blok manual.
4. Klik blok untuk edit di panel kanan (tab Properti & Advanced).
5. Atur **⚙️ Pengaturan** untuk SEO, tema warna, dark mode, animasi, dan Supabase.
6. Simpan project (💾), Export ZIP (📦), atau Download HTML (⬇️).

## Fitur lengkap
- **26 blok**: Hero, Section, Kolom, Heading, Teks, Gambar, Tombol, List, Kartu, Fitur, CTA, Pricing, Testimoni, Accordion/FAQ, Galeri, Statistik, Form, Form→Supabase, Booking/Reservasi, Order via WhatsApp, Video, Peta, Footer, Custom HTML, Spacer, Divider.
- **✨ AI Generate** offline — deteksi jenis situs + tema dari teks.
- **SEO/Meta** — description, keywords, Open Graph, Twitter card, favicon, Google Analytics.
- **Tema preset** (6) + **Dark mode** + **Animasi scroll**.
- **Multi-halaman** dengan navigasi otomatis antar halaman.
- **Export ZIP** (semua halaman + README, siap upload hosting).
- **Simpan/Muat** project (browser) + Export/Import `.json`.
- **Mode Advanced** (ID, class, inline-style per blok).
- **Undo/Redo**, preview Desktop/Tablet/HP, pencarian blok.
- **Lisensi hybrid** (hash, opsi online-check).

## Untuk MENJUAL — yang perlu Anda ubah di kode
Buka file dengan editor teks, cari bagian ini di dalam `<script>`:

1. **Ganti kunci lisensi** — cari `VALID_HASHES`. Setiap kunci punya hash. Untuk membuat kunci baru:
   - Tentukan kunci (mis. `PEMBELI-001`).
   - Hitung hash-nya dengan algoritma djb2 (saya bisa bantu generate), lalu masukkan ke array `VALID_HASHES`.
   - Kunci asli TIDAK tersimpan di file, jadi pembeli tidak bisa menebaknya dari source.
2. **(Opsional) Online check** — isi `LICENSE_SERVER` dengan endpoint Anda yang mengembalikan `{valid:true}`. Ini mencegah 1 kunci dipakai banyak orang.
3. **(Opsional) Branding** — ganti teks "BlokBuild" dengan merek Anda.

## Catatan keamanan jujur
Versi ini menyembunyikan kunci (hash) sehingga aman untuk distribusi normal. Untuk proteksi maksimal terhadap pembajakan tingkat lanjut, validasi sebaiknya dipindah ke server (set `LICENSE_SERVER`). File tetap berfungsi penuh tanpa server.
