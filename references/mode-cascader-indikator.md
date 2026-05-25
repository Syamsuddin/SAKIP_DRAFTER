# Mode CASCADER — Panduan Penurunan Kinerja Antar Level

## Prinsip Cascading yang Benar

### 1. Hubungan Logis (Bukan Hirarkis Formal)
Cascading BUKAN sekedar "atasan menulis outcome, bawahan menulis output."
Cascading adalah **rantai kausalitas**: output level bawah MENYEBABKAN
tercapainya outcome level atas.

```
Outcome (Eselon II): Meningkatnya Kualitas Pelayanan Publik OPD
                              ↑ (didukung oleh)
Output (Eselon III): Persentase Layanan yang Diselesaikan Tepat Waktu
                              ↑ (dihasilkan dari)
Sub-output (Eselon IV): Jumlah SDM Pelayanan yang Terlatih
```

### 2. Aturan Anti Copy-Paste
- IKU level bawah TIDAK BOLEH sama dengan IKU level atas
- IKU level bawah HARUS lebih spesifik/operasional
- Satu IKU atasan dapat diturunkan menjadi 2–4 IKU bawahan

### 3. Formula Kontribusi
Jika IKU atasan adalah gabungan dari beberapa IKU bawahan:
```
Target Atasan = f(Target Bawahan 1, Target Bawahan 2, ...)
```
Pastikan target bawahan, jika dicapai semua, akan menghasilkan target atasan.

---

## Prosedur Cascading

### Input yang Dibutuhkan
1. IKU dan target level atas (minimal 1 level di atas yang akan di-cascade)
2. Struktur organisasi OPD (eselon dan nama jabatan)
3. Tupoksi setiap unit (bidang, seksi, subbagian)
4. Program/kegiatan/sub-kegiatan yang menjadi tanggung jawab setiap unit

### Langkah Cascading

**Langkah 1: Dekomposisi IKU Atasan**
Untuk setiap IKU atasan, identifikasi:
- Apa proses/aktivitas yang menghasilkan outcome ini?
- Unit mana yang paling berkontribusi?
- Bagaimana cara mengukur kontribusi masing-masing unit?

**Langkah 2: Penugasan IKU ke Unit**
- Setiap bidang/seksi mendapat IKU yang sesuai dengan tupoksinya
- Pastikan tidak ada tupoksi yang tidak tercermin dalam IKU
- Hindari penugasan IKU yang sama ke lebih dari satu unit

**Langkah 3: Penetapan Target Kontribusi**
- Target setiap unit harus proporsional terhadap target atasan
- Gunakan data historis atau estimasi berbasis kapasitas

**Langkah 4: Validasi Logika**
- Simulasikan: jika semua unit mencapai target, apakah target atasan tercapai?
- Jika tidak, revisi target atau tambahkan unit

---

## Template Output Cascading

### Format Tabel Cascading
```
## MATRIKS CASCADING KINERJA
### [Nama OPD] — Tahun [Tahun]

| Level | Jabatan | Sasaran Strategis | IKU | Satuan | Target | Sumber Data |
|---|---|---|---|---|---|---|
| Outcome | Kepala OPD (Eselon II) | ... | ... | ... | ... | ... |
| Output | Kabid [A] (Eselon III) | ... | ... | ... | ... | ... |
| Output | Kabid [B] (Eselon III) | ... | ... | ... | ... | ... |
| Sub-output | Kasi [A1] (Eselon IV) | ... | ... | ... | ... | ... |
| Sub-output | Kasi [A2] (Eselon IV) | ... | ... | ... | ... | ... |
```

---

## Contoh Cascading Dinas Kesehatan

| Level | Jabatan | IKU | Target |
|---|---|---|---|
| Outcome | Kepala Dinas | Angka Harapan Hidup | 70,5 tahun |
| Output | Kabid Kesmas | % Desa dengan Posyandu Aktif | 85% |
| Output | Kabid Yankes | % Puskesmas Terakreditasi | 100% |
| Output | Kabid P2P | Angka Kesakitan DBD per 100.000 penduduk | ≤ 49 |
| Sub-output | Kasi Gizi | % Balita Stunting | ≤ 14% |
| Sub-output | Kasi Promkes | % RT dengan PHBS | 75% |

---

---

# Mode INDIKATOR — Panduan Perancangan IKU/IKK

## Kriteria SMART-C untuk Indikator

| Kriteria | Definisi | Pertanyaan Uji |
|---|---|---|
| **S**pesifik | Menggambarkan satu hal yang jelas | "Apakah indikator ini hanya bisa diartikan satu cara?" |
| **M**easurable | Dapat diukur secara objektif | "Apakah ada metode pengukuran yang jelas?" |
| **A**chievable | Target dapat dicapai | "Apakah realistis dengan sumber daya yang ada?" |
| **R**elevant | Relevan dengan tupoksi | "Apakah OPD memiliki kendali atas indikator ini?" |
| **T**ime-bound | Terikat waktu | "Kapan diukurnya? Tahunan? Triwulanan?" |
| **C**onsistent | Selaras dengan level di atas | "Apakah berkontribusi terhadap IKU atasan?" |

---

## Tipologi Indikator dan Penerapannya

### Impact (Dampak)
- **Definisi**: Perubahan jangka panjang pada masyarakat/lingkungan
- **Level**: RPJMD, Renstra lintas OPD
- **Contoh baik**: IPM, Angka Kemiskinan, Indeks Gini
- **Contoh buruk**: "Meningkatnya kegiatan pemberdayaan masyarakat"

### Outcome (Hasil)
- **Definisi**: Perubahan perilaku/kondisi sasaran akibat intervensi OPD
- **Level**: Renstra OPD, PK Eselon II
- **Contoh baik**: "Persentase UMKM yang mengalami peningkatan omzet ≥10%"
- **Contoh buruk**: "Jumlah pelatihan UMKM yang dilaksanakan"

### Output (Keluaran)
- **Definisi**: Produk langsung dari kegiatan OPD
- **Level**: Renja, PK Eselon III–IV
- **Contoh baik**: "Jumlah UMKM yang mendapatkan sertifikasi halal"
- **Contoh buruk**: "Terlaksananya kegiatan sertifikasi halal"

### Process (Proses)
- **Definisi**: Tahapan pelaksanaan kegiatan
- **Level**: SKP ASN (bukan IKU OPD)
- **Contoh**: "Jumlah laporan monitoring yang diselesaikan tepat waktu"

---

## Panduan Merancang IKU dari Nol

### Langkah 1: Tentukan Sasaran Strategis
Rumuskan sasaran dengan pola: [Kata kerja hasil] + [Objek] + [Spesifikasi]
- Contoh: "Meningkatnya Kualitas Infrastruktur Jalan di Wilayah Perdesaan"

### Langkah 2: Identifikasi Dimensi yang Bisa Diukur
Untuk setiap sasaran, tanyakan:
- Dari sisi **kuantitas**: Berapa banyak?
- Dari sisi **kualitas**: Seberapa baik?
- Dari sisi **ketepatan waktu**: Seberapa cepat?
- Dari sisi **cakupan**: Berapa persen yang terlayani?

### Langkah 3: Pilih Satuan yang Tepat
| Tipe Pengukuran | Satuan yang Direkomendasikan |
|---|---|
| Proporsi/Cakupan | Persentase (%) |
| Absolut | Unit, Orang, Km, Ha, dsb |
| Skala/Indeks | Indeks (0–100 atau 1–4) |
| Rasio | Per 1.000, Per 100.000 |
| Waktu | Hari, Jam |

### Langkah 4: Verifikasi Sumber Data
Setiap IKU HARUS memiliki sumber data yang jelas:
- Data primer OPD (laporan internal, sistem aplikasi)
- Data BPS (Susenas, Podes, SP, dll.)
- Data K/L teknis (Kemenkes, Kemendikbud, dll.)
- Survei kepuasan (IKM)

### Langkah 5: Uji SMART-C
Gunakan tabel kriteria SMART-C di atas untuk menguji setiap IKU yang diusulkan.

---

## Bank Indikator per Bidang Urusan

### Urusan Pendidikan (Dinas Pendidikan)
| Tingkatan | IKU | Satuan |
|---|---|---|
| Outcome | Angka Rata-Rata Lama Sekolah | Tahun |
| Outcome | Angka Harapan Lama Sekolah | Tahun |
| Output | Persentase Sekolah Terakreditasi Minimal B | % |
| Output | Angka Partisipasi Murni SD/SMP | % |
| Output | Persentase Guru Bersertifikat Pendidik | % |

### Urusan Kesehatan (Dinas Kesehatan)
| Tingkatan | IKU | Satuan |
|---|---|---|
| Outcome | Angka Harapan Hidup | Tahun |
| Outcome | Angka Kematian Ibu (AKI) | Per 100.000 KH |
| Outcome | Angka Kematian Bayi (AKB) | Per 1.000 KH |
| Output | Persentase Balita Stunting | % |
| Output | Persentase Puskesmas Terakreditasi | % |
| Output | Persentase Desa/Kelurahan dengan Posyandu Aktif | % |

### Urusan PU dan Penataan Ruang
| Tingkatan | IKU | Satuan |
|---|---|---|
| Outcome | Persentase Jalan dalam Kondisi Baik | % |
| Outcome | Persentase Rumah Tangga dengan Akses Air Minum Layak | % |
| Output | Panjang Jalan yang Dibangun/Ditingkatkan | Km |
| Output | Jumlah Infrastruktur Irigasi yang Direhabilitasi | Unit |

### Urusan Sosial (Dinas Sosial)
| Tingkatan | IKU | Satuan |
|---|---|---|
| Outcome | Persentase PMKS yang Tertangani | % |
| Outcome | Penurunan Angka Kemiskinan | % |
| Output | Persentase KPM PKH yang Graduasi Mandiri | % |
| Output | Jumlah PSKS yang Aktif | Orang/Lembaga |

### Urusan Pertanian (Dinas Pertanian)
| Tingkatan | IKU | Satuan |
|---|---|---|
| Outcome | Nilai Tukar Petani (NTP) | Indeks |
| Outcome | Produksi Padi | Ton |
| Output | Luas Lahan yang Mendapat Bantuan Pupuk | Ha |
| Output | Jumlah Kelompok Tani yang Dibina | Kelompok |

---

## Indikator yang DILARANG sebagai IKU OPD

Berikut contoh indikator yang sering muncul namun TIDAK BOLEH dijadikan IKU:

| Indikator Bermasalah | Masalah | Alternatif yang Benar |
|---|---|---|
| "Jumlah rapat yang dilaksanakan" | Proses, bukan hasil | "Persentase keputusan rapat yang ditindaklanjuti" |
| "Jumlah perjalanan dinas" | Aktivitas/input | "Persentase tujuan perjalanan dinas yang tercapai" |
| "Tersusunnya dokumen perencanaan" | Keluaran administratif | "Nilai evaluasi SAKIP OPD" |
| "Terlaksananya kegiatan X" | Konfirmasi aktivitas | "Persentase target kegiatan X yang tercapai" |
| "Jumlah anggaran yang terserap" | Input (bukan hasil) | "Persentase program yang mencapai target output" |
