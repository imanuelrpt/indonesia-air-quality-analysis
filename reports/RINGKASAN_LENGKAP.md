# Analisis Kualitas Udara Indonesia
## Kualitas Udara Provinsi (IKU/IKLH 2020-2024) & Studi Kasus Harian DKI Jakarta (ISPU 2024-2025)

### Ringkasan Eksekutif
Kualitas udara Indonesia menunjukkan perbaikan yang konsisten selama 2020-2024: rata-rata IKU
provinsi naik **+3.06 poin** (88.27 -> 91.33) dan IKLH komposit +4.09 poin,
tetapi perbaikan itu tidak merata - provinsi Jawa mencatat IKU terendah (82.06) sementara Papua
tertinggi (95.00), dan kualitas udara berkorelasi negatif dengan kepadatan penduduk
(Pearson r = **-0.67**, p < 0,001, n = 34). Untuk kondisi terkini pada skala harian, studi kasus
DKI Jakarta (3,480 pengamatan ISPU, Januari 2024 - November 2025, 5 stasiun) menunjukkan rata-rata ISPU
**73.4** (kategori *Sedang*): 77% hari *Sedang* dan 9.8% hari *Tidak Sehat*, dengan
**PM2.5 sebagai pencemar kritis pada 86% hari**. Semua kota administrasi Jakarta berada di bawah
rata-rata nasional versi IKU.

### Insight
1. **Tren nasional membaik.** IKU rata-rata provinsi naik dari 88.27 (2020) ke 91.33 (2024), +3.06 poin; IKLH +4.09 poin.
2. **Kesenjangan wilayah mencolok.** Rata-rata IKU 2024: Jawa 82.06 (terendah) vs Papua 95.00 (tertinggi). Lima dari enam provinsi Jawa masuk 10 terburuk.
3. **Provinsi terbaik & terburuk 2024.** Terbaik KALIMANTAN SELATAN (96.41); terburuk BANTEN (69.84) - selisih 26.57 poin.
4. **Korelasi kepadatan penduduk.** IKU 2024 vs kepadatan (2021): r = -0.67 (p < 0,001). Hubungan negatif sedang-kuat: provinsi lebih padat cenderung ber-IKU lebih rendah. **Korelasi, bukan kausalitas.**
5. **Dinamika berlawanan di Jawa.** JAWA BARAT membaik +5.18 poin (2020-2024), sementara BANTEN justru memburuk -2.96 poin - satu-satunya provinsi Jawa yang turun.
6. **Jakarta (IKU tahunan): disparitas internal besar.** Rata-rata 5 kota adm 2024 = 68.55, di bawah nasional (91.33). Jakarta Timur melonjak +22.92 poin (ke 71.16), Jakarta Utara +19.04, tetapi Jakarta Pusat memburuk -4.22 (ke 64.94).
7. **Jakarta (ISPU harian 2024-2025): hampir selalu "Sedang".** Dari 3,480 hari-stasiun valid: **Sedang 77.4%** (2,694), **Baik 12.8%** (444), **Tidak Sehat 9.8%** (341), **Sangat Tidak Sehat 1 hari**. Rata-rata ISPU 73.4; 2024 (75.1) cenderung lebih buruk daripada 2025 Jan-Nov (71.5).
8. **Pencemar kritis didominasi PM2.5.** PM2.5 menjadi parameter kritis pada **86.0%** hari, disusul SO2 (6.5%) dan PM10 (5.1%). Artinya masalah Jakarta bukan SO2/NO2 (basis IKU), melainkan partikulat halus.
9. **Barat terburuk, Timur terbaik.** Rata-rata ISPU & % hari Tidak Sehat: Jakarta Barat **76.6** (16.3%) tertinggi; Jakarta Timur **70.8** terendah. Hari ekstrem: Jakarta Selatan ISPU 202 (Sangat Tidak Sehat).
10. **Pola musiman kuat, akhir pekan tidak berbeda.** ISPU memuncak pada musim kemarau (Jun 2025 = 94.8) dan terendah pada musim hujan (Jan 2025 = 48.1). Rata-rata hari kerja (73.36) hampir identik dengan akhir pekan (73.37) - lalu lintas bukan satu-satunya penggerak.

### Rekomendasi
1. **Prioritaskan PM2.5.** Karena 86% hari kritis disebabkan PM2.5, intervensi harus menyasar sumber partikulat (transportasi diesel, pembakaran, industri), bukan hanya NO2/SO2.
2. **Fokuskan wilayah Jakarta Barat** yang mencatat ISPU rata-rata dan frekuensi hari Tidak Sehat tertinggi.
3. **Lanjutkan pemantauan harian:** ISPU harian mengungkap episode yang tak terlihat pada IKU tahunan; pertahankan minimal 5 SPKU dan publikasi terbuka.
4. **Antisipasi musim kemarau (Mei-Oktober):** siapkan peringatan dini dan pembatasan sumber emisi pada bulan puncak.
5. **Perkuat wilayah padat nasional:** perluas transportasi publik, uji emisi, dan pengawasan kawasan industri di BANTEN, DKI JAKARTA, dan JAWA BARAT.
6. **Perluas metrik resmi:** jika memungkinkan, masukkan PM2.5/PM10 ke dalam IKU nasional agar selaras dengan risiko kesehatan.

### Keterbatasan
- **Dua metrik berbeda, tidak dicampur.** IKU (skala 0-100, **makin tinggi makin baik**, dari NO2 & SO2, **tahunan**) != ISPU (skala 0-500+, **makin tinggi makin buruk**, **harian**).
- **Periode ISPU berakhir 30 November 2025**; belum ada data 2026 pada sumber resmi. Nilai 2025 bersifat Januari-November.
- **Cakupan ISPU terbatas 5 stasiun** (DKI1-DKI5) mewakili 5 kota administrasi; Kab. Adm. Kepulauan Seribu tanpa stasiun tetap.
- **Kualitas data:** 13 baris bernilai ISPU 0 tanpa polutan apa pun adalah placeholder "tidak ada data" (dikosongkan); 20 dari 3.500 baris ISPU kosong; 1 stasiun-hari duplikat dibuang.
- **Kepadatan penduduk hanya 2021** dan 34 provinsi lama.
- **Kendaraan bermotor tidak dianalisis** (data tidak dapat diotomatisasi dari sumber publik).
- 15 dari 514 kab/kota gagal diekstrak dari PDF sumber.
- Analisis korelasi **tidak** membuktikan hubungan sebab-akibat.

### Draft LinkedIn (<=150 kata)
Kualitas udara Indonesia membaik, tapi belum merata. Saya menganalisis data resmi KLHK, BPS, dan
Satu Data Jakarta dengan Python (pandas, matplotlib, scipy).

IKU provinsi naik +3.06 poin (2020-2024), namun Jawa tetap terendah (82.1) vs Papua (95.0);
IKU berkorelasi negatif dengan kepadatan penduduk (r = -0.67, p < 0,001). Di DKI Jakarta, saya mengolah
3,480 pengamatan ISPU harian (2024-Nov 2025, 5 stasiun): rata-rata 73.4 (kategori Sedang) - 77% hari
Sedang, 9.8% Tidak Sehat, dan PM2.5 menjadi pencemar kritis pada 86% hari. Jakarta Barat terburuk;
polusi memuncak saat kemarau (Jun 2025) dan tak berbeda antara hari kerja dan akhir pekan.

Perbaikan nasional nyata, tetapi kota padat tetap jadi tantangan utama. Korelasi bukan kausalitas.

#DataAnalytics #Python #KualitasUdara #Lingkungan

### Poin CV
- Menganalisis kualitas udara **38 provinsi (IKU/IKLH 2020-2024)** dan **3,480 pengamatan ISPU harian DKI Jakarta (2024-2025)** dari sumber resmi KLHK, BPS, dan Satu Data Jakarta; melakukan ekstraksi PDF serta parsing API/tabel JavaScript dengan Python (pdfplumber, requests, pandas).
- Membangun pipeline data 3 tahap (collection, cleaning, EDA) dengan verifikasi silang dua sumber (selisih IKU <= 0,03 poin) dan dokumentasi sumber data lengkap.
- Menemukan korelasi negatif kepadatan penduduk-IKU 2024 (r = -0.67, p < 0,001) serta mengidentifikasi **PM2.5 sebagai pencemar kritis pada 86% hari** di Jakarta; menyajikan **12 visualisasi** dan rekomendasi berbasis data.
