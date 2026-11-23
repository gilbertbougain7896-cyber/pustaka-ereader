# Pustaka Ereader

Katalog buku ramah e-reader. Berjalan di GitHub Pages, tanpa server.

## Isi
- `index.html`  situs lengkap (satu file)
- `data/books.json`  daftar buku (18 buku contoh, tanpa berkas)
- `books/<id>/`  berkas buku (EPUB, AZW3, PDF) yang kamu unggah lewat admin

## Pasang di GitHub Pages
1. Buat repo publik baru di GitHub (misalnya `pustaka-ereader`).
2. Unggah semua isi folder ini ke cabang `main`.
3. Repo > Settings > Pages > Build and deployment > Deploy from a branch > `main` / `(root)` > Save.
4. Tunggu sekitar satu menit. Alamatnya `https://NAMAKAMU.github.io/pustaka-ereader/`.

Situs mengenali nama akun dan repo dari alamatnya sendiri. Kalau pakai domain sendiri, tambahkan baris ini di `index.html` sebelum `<script>` utama:
`<script>window.PT_CONFIG={owner:'NAMAKAMU',repo:'pustaka-ereader'}</script>`

## Buat token untuk admin
1. GitHub > Settings > Developer settings > Personal access tokens > Fine-grained tokens > Generate new token.
2. Repository access: pilih **Only select repositories**, lalu repo ini saja.
3. Permissions > Repository permissions: **Contents: Read and write** dan **Issues: Read and write**.
4. Generate, lalu salin token (`github_pat_...`).
5. Buka `#admin-unggah` di situsmu, tempel token, klik Sambungkan.

Token hanya disimpan di browser yang kamu pakai. Jangan bagikan token. Tanpa token, pengunjung hanya bisa membaca katalog.

## Alur harian
- **Tambah buku**: Admin > Unggah buku > pilih EPUB. Judul, penulis, tahun, dan pratinjau terisi otomatis. Isi genre dan jumlah halaman, centang "Sudah dites", lalu Terbitkan.
- **Ubah status / hapus**: Admin > Katalog.
- **Laporan**: pengunjung mengirim lewat GitHub Issues (judul berawalan `[Laporan]`). Kamu tindak lanjuti di Admin > Laporan.
- Setelah menyimpan, situs publik diperbarui sekitar satu menit.

## Hapus buku contoh
18 buku contoh belum punya berkas unduhan. Hapus lewat Admin > Katalog saat kamu sudah punya buku sendiri.

## Batasan
- Satu berkas maksimal 100 MB, dan repo sebaiknya di bawah 1 GB.
- Pelapor butuh akun GitHub.
- Hanya unggah buku domain publik atau berlisensi bebas.
