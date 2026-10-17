# DATA_SOURCES

Dokumen ini mencatat seluruh sumber data yang digunakan dalam proyek **Analisis Kualitas Udara di Indonesia**. Setiap file mentah di `data/raw/` harus dapat dilacak ke sumber di bawah ini.

Tanggal unduh terakhir: **2026-10-17**

| No | File lokal | Judul tabel/dataset | Subjek | Periode | Sumber (URL) | Tanggal unduh | Lisensi | Catatan definisi |
|----|------------|---------------------|--------|---------|--------------|---------------|---------|------------------|
| 1 | `KLHK_Statistik_Lingkungan_Hidup_Vol1_2025.pdf` | Statistik Kementerian Lingkungan Hidup / Badan Pengendalian Lingkungan Hidup 2024 (Volume I) | Publikasi statistik lingkungan hidup (udara, air, lahan, sampah, dll.) | s.d. 2024 | https://statistik.kemenlh.go.id/admin-office/storage/publikasi/statistik-lingkungan-hidup-volume-i-tahun-2025.pdf | 2026-10-17 | Tidak dicantumkan (data pemerintah, wajib atribusi) | Publikasi resmi KLHK. Berisi Tabel 2.1 (IKLH), 2.10 (IKU Provinsi), 2.11 (IKU Kab/Kota). 476 halaman. |
| 2 | `klhk_iku_provinsi_2020_2024.csv` | Tabel 2.10 Indeks Kualitas Udara (IKU) Provinsi Tahun 2020–2024 | Indeks Kualitas Udara per provinsi (38 provinsi + Nasional) | 2020–2024 | Diekstrak dari file No. 1 (hlm. cetak 134–135 / PDF 144–145) | 2026-10-17 | Tidak dicantumkan | IKU = indeks kualitas udara ambien yang dihitung dari parameter **NO₂** dan **SO₂** (Sumber: Direktorat Perlindungan dan Pengelolaan Mutu Udara). Skala 0–100, makin tinggi makin baik. Provinsi baru (Papua Selatan/Tengah/Pegunungan, Papua Barat Daya) hanya tersedia sejak 2023. |
| 3 | `klhk_iklh_provinsi_2020_2024.csv` | Tabel 2.1 Indeks Kualitas Lingkungan Hidup (IKLH) Provinsi Tahun 2020–2024 | IKLH komposit per provinsi (38 provinsi + Nasional) | 2020–2024 | Diekstrak dari file No. 1 (hlm. cetak 73–74 / PDF 83–84) | 2026-10-17 | Tidak dicantumkan | IKLH = indeks gabungan IKA (air) + IKU (udara) + IKL/IKTL (lahan). Nama provinsi di PDF memakai "Nanggroe Aceh Darussalam" dan "Daerah Istimewa Yogyakarta"; dinormalisasi ke "ACEH" dan "DI YOGYAKARTA". |
| 4 | `klhk_iku_kabkota_2020_2024.csv` | Tabel 2.11 Indeks Kualitas Udara (IKU) Kabupaten/Kota Tahun 2020–2024 | IKU per kabupaten/kota (nasional) | 2020–2024 | Diekstrak dari file No. 1 (hlm. cetak 136–174 / PDF 146–184) | 2026-10-17 | Tidak dicantumkan | 499 baris terekstrak dari 514 baris pada tabel asli (≈97%). Selisih akibat nama kabupaten/kota yang terpecah antar baris pada PDF. Semua kota besar target studi kasus (Jakarta, Surabaya, Bandung, Medan, Semarang, Makassar, Denpasar, Palembang, Bekasi, Tangerang, Depok) terverifikasi ada. Kolom `ekoregion`: Sumatera, Jawa, Kalimantan, Sulawesi, Balinusra, Ambon, Papua. |
| 5 | `bps_komponen_iklh_provinsi_2024.csv` | Komponen Penyusun Indeks Kualitas Lingkungan Hidup Menurut Provinsi | Komponen IKLH: IKU, IKA, IKTL, IKL, IKEG, IKAL per provinsi (38 + Indonesia) | 2024 | https://www.bps.go.id/id/statistics-table/2/MjUzMiMy/komponen-penyusun-indeks-kualitas-lingkungan-hidup-menurut-provinsi.html | 2026-10-17 | Tidak dicantumkan (wajib atribusi) | Sumber data: Kementerian Lingkungan Hidup. Digunakan sebagai **verifikasi silang** nilai IKU 2024. Contoh: IKU Indonesia 2024 = 90,13 (BPS) vs 90,10 (KLHK, pembulatan); Sumatera Utara 92,26 di kedua sumber. |
| 6 | `bps_kepadatan_penduduk_provinsi_2021.csv` | Kepadatan Penduduk menurut Provinsi | Kepadatan penduduk (jiwa/km²) per provinsi | 2021 | https://www.bps.go.id/id/statistics-table/2/MTQxIzI=/kepadatan-penduduk-menurut-provinsi.html | 2026-10-17 | Tidak dicantumkan (wajib atribusi) | Faktor penjelas (explanatory). 35 baris (34 provinsi lama + Indonesia); provinsi hasil pemekaran Papua (2022) belum ada. Hanya tahun 2021 tersedia pada endpoint ini. |
| 7 | `jakarta_ispu_harian_2024_2025.csv` | Data Indeks Standar Pencemar Udara (ISPU) di Provinsi DKI Jakarta | ISPU **harian** per stasiun pemantau (5 stasiun) | Jan 2024 – Nov 2025 | https://satudata.jakarta.go.id/open-data/detail?kategori=dataset&page_url=data-indeks-standar-pencemar-udara-ispu-di-provinsi-dki-jakarta | 2026-10-17 | Tidak dicantumkan (data pemerintah DKI, wajib atribusi) | Sumber: Dinas Lingkungan Hidup DKI Jakarta, portal Satu Data Jakarta. 3.501 baris ditarik otomatis via API `POST https://satudata.jakarta.go.id/backend/api/v2/satudata/detail` (paginasi `data_no`, `per_page` maks 100). Kolom: `periode_data, bulan, tanggal, stasiun, pm_sepuluh, pm_duakomalima, sulfur_dioksida, karbon_monoksida, ozon, nitrogen_dioksida, max, parameter_pencemar_kritis, kategori`; `max` = nilai ISPU harian. Data terakhir diperbarui portal 2026-06-05, tetapi **isi data berhenti di Nov 2025**. |

## Parameter baku mutu (referensi kategori ISPU)

Kategori Indeks Standar Pencemar Udara (ISPU), **Permen LHK No. 14 Tahun 2020**:

| Rentang ISPU | Kategori |
|--------------|----------|
| 1–50 | Baik |
| 51–100 | Sedang |
| 101–200 | Tidak Sehat |
| 201–300 | Sangat Tidak Sehat |
| ≥301 | Berbahaya |

> Catatan: **IKU** (Indeks Kualitas Udara, skala 0–100, makin tinggi makin baik) berbeda dari **ISPU** (skala 0–500+, makin tinggi makin buruk). Keduanya tidak boleh dicampur dalam satu analisis.

## Sumber yang dipertimbangkan tetapi TIDAK digunakan

| Sumber | Alasan tidak dipakai |
|--------|----------------------|
| SISKLHK KLHK `statistik.menlhk.go.id` / `statistik.kemenlh.go.id/sisklhkX` | Tabel dirender via API internal tanpa endpoint data publik (halaman HTML mengembalikan shell 404). Digantikan oleh PDF resmi KLHK. |
| Satu Data KLHK (`satudata.kemenlh.go.id`) | Katalog metadata hidup (107 dataset, termasuk IKU 2024 & indikator 2025), tetapi **unduhan berkas biner mengembalikan 404 "Isi berkas biner tidak tersedia"**. Tidak ada IKU tahunan 2025 yang dapat diunduh. |
| CKAN Surabaya (`ckan.surabaya.go.id`) | Metadata API hidup, tetapi endpoint unduh CSV mengembalikan HTTP 500. |
| OpenAQ (`api.openaq.org` v3) | Butuh API key (401 tanpa key). Arsip S3 publik tanpa metadata lokasi, sehingga kota tak bisa dipetakan. |
| AQICN | Data historis butuh akun gratis. |
| Portal ISPU KLHK (`ispu.kemenlh.go.id/webv5`) | Hanya menyediakan **snapshot real-time** (endpoint `/stasiun`), tidak ada data historis. |
| NASA FIRMS / hotspot karhutla | Butuh login Earthdata (ditunda sesuai keputusan pengguna). |
| BPS tabel "Jumlah Kendaraan Bermotor Menurut Provinsi" (tipe `statistics-table/3/`) | Data tidak disematkan di HTML; di-load via `web-api.bps.go.id` yang tidak mengekspos endpoint publik tanpa kunci. Perlu unduh manual (rencana tindak lanjut). |

## Skema kolom tiap CSV

- `klhk_iku_provinsi_2020_2024.csv`: `provinsi`, `provinsi_raw`, `2020`, `2021`, `2022`, `2023`, `2024`
- `klhk_iklh_provinsi_2020_2024.csv`: `provinsi`, `provinsi_raw`, `2020`, `2021`, `2022`, `2023`, `2024`
- `klhk_iku_kabkota_2020_2024.csv`: `nama`, `2020`, `2021`, `2022`, `2023`, `2024`, `ekoregion`
- `bps_komponen_iklh_provinsi_2024.csv`: `provinsi`, `Indeks Kualitas Udara`, `Indeks Kualitas Air`, `Indeks Kualitas Tutupan Lahan (IKTL)`, `Indeks Kualitas Lahan (IKL)`, `Indeks Kualitas Ekosistem Gambut (IKEG)`, `Indeks Kualitas Air Laut (IKAL)`
- `bps_kepadatan_penduduk_provinsi_2021.csv`: `provinsi`, `tahun`, `kepadatan_penduduk`
- `jakarta_ispu_harian_2024_2025.csv` (mentah): `periode_data`, `bulan`, `tanggal`, `stasiun`, `pm_sepuluh`, `pm_duakomalima`, `sulfur_dioksida`, `karbon_monoksida`, `ozon`, `nitrogen_dioksida`, `max`, `parameter_pencemar_kritis`, `kategori`
- `jakarta_ispu_harian_clean.csv` (olahan): `tanggal_dt`, `periode_data`, `kode_stasiun`, `stasiun`, `kota_adm`, `pm_sepuluh`, `pm_duakomalima`, `sulfur_dioksida`, `karbon_monoksida`, `ozon`, `nitrogen_dioksida`, `ispu`, `kategori`, `kategori_rank`, `polutan_kritis`
