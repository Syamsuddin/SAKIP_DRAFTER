# Mode REVIEWER — Panduan Analisis dan Penilaian Dokumen SAKIP

## Alur Kerja Review

1. Identifikasi jenis dokumen yang diberikan pengguna
2. Jalankan checklist standar untuk jenis dokumen tersebut
3. Identifikasi kelemahan spesifik
4. Berikan rekomendasi perbaikan yang konkret dan actionable
5. Tampilkan ringkasan penilaian dalam tabel

---

## Checklist Review per Dokumen

### Review Renstra OPD

**A. Kesesuaian Struktur (Permendagri 86/2017)**
- [ ] Memiliki 8 bab sesuai ketentuan
- [ ] Setiap bab memuat substansi yang diwajibkan
- [ ] Terdapat matriks tujuan-sasaran-indikator-target

**B. Kualitas Tujuan dan Sasaran**
- [ ] Tujuan OPD selaras dengan tujuan/sasaran RPJMD
- [ ] Sasaran bersifat hasil (outcome), bukan aktivitas
- [ ] Setiap tujuan minimal memiliki 1 sasaran
- [ ] Rumusan sasaran menggunakan kata kerja hasil: "Meningkat", "Menurun", "Terwujud"

**C. Kualitas Indikator**
- [ ] Setiap sasaran memiliki minimal 1 IKU
- [ ] IKU bersifat outcome, bukan output/input
- [ ] IKU dapat diukur secara objektif (ada sumber data)
- [ ] Tidak ada indikator yang bersifat aktivitas (contoh buruk: "Jumlah rapat koordinasi")
- [ ] Satuan indikator jelas (%, orang, unit, indeks)

**D. Kualitas Target**
- [ ] Target tahunan bersifat progresif (meningkat/menurun sesuai arah)
- [ ] Target realistis (tidak terlalu tinggi/rendah tanpa justifikasi)
- [ ] Terdapat kondisi awal (baseline) sebagai dasar penetapan target
- [ ] Kondisi akhir periode sesuai target RPJMD

**E. Konsistensi Internal**
- [ ] Indikator di tabel tujuan konsisten dengan tabel sasaran
- [ ] Nomenklatur program sesuai Kepmendagri 050-5889/2021
- [ ] Tidak ada kontradiksi antar bab

---

### Review Perjanjian Kinerja (PK)

**A. Kelengkapan Format**
- [ ] Terdapat identitas pejabat dan atasan lengkap
- [ ] Terdapat pernyataan perjanjian
- [ ] Terdapat tabel sasaran strategis dengan IKU dan target
- [ ] Terdapat tabel program/kegiatan dengan anggaran
- [ ] Terdapat tanda tangan kedua pihak dan tanggal

**B. Kualitas Konten**
- [ ] Sasaran strategis selaras dengan Renstra/Renja
- [ ] IKU di PK konsisten dengan IKU di Renstra
- [ ] Target PK konsisten dengan target tahunan di Renstra
- [ ] Seluruh program/kegiatan memiliki anggaran yang jelas
- [ ] Tidak ada duplikasi sasaran atau IKU

**C. Cascading (jika PK di bawah Eselon II)**
- [ ] IKU merupakan turunan logis dari IKU atasan
- [ ] Target berkontribusi terhadap pencapaian target atasan
- [ ] Tidak ada IKU yang sama persis dengan IKU atasan (copy-paste)

---

### Review LKIP/LAKIP

**A. Kelengkapan Struktur**
- [ ] Terdapat ringkasan eksekutif
- [ ] Memiliki 4 bab sesuai PermenPAN-RB 53/2014
- [ ] Terdapat lampiran (PK, pengukuran kinerja, dll.)

**B. Kualitas Pengukuran Kinerja**
- [ ] Setiap IKU dianalisis secara individual
- [ ] Formula capaian digunakan dengan benar
- [ ] Terdapat perbandingan dengan tahun sebelumnya
- [ ] Terdapat perbandingan dengan target akhir Renstra
- [ ] Tidak ada IKU yang tidak diukur/dianalisis

**C. Kualitas Analisis**
- [ ] Analisis menjelaskan PENYEBAB, bukan sekadar mengulang angka
- [ ] Disebutkan program/kegiatan yang mendukung capaian
- [ ] Hambatan dijelaskan secara spesifik
- [ ] Terdapat upaya konkret yang sudah/akan dilakukan
- [ ] Efisiensi penggunaan anggaran dianalisis

**D. Akuntabilitas Anggaran**
- [ ] Realisasi anggaran per program/kegiatan tersaji
- [ ] Efisiensi/inefisiensi dianalisis
- [ ] Terdapat korelasi antara realisasi anggaran dan capaian kinerja

---

## Kesalahan Umum SAKIP (Red Flags)

### Kesalahan Fatal (Harus Diperbaiki)
| Kode | Kesalahan | Contoh | Perbaikan |
|---|---|---|---|
| F01 | IKU bersifat aktivitas | "Jumlah rapat yang dilaksanakan" | Ganti dengan hasil rapat: "Persentase rekomendasi rapat yang ditindaklanjuti" |
| F02 | Cascading copy-paste | IKU eselon III sama dengan eselon II | Turunkan menjadi output yang mendukung outcome atasan |
| F03 | Target tanpa baseline | Target naik 50% tanpa data awal | Sertakan data baseline dari tahun sebelumnya |
| F04 | Indikator tidak terukur | "Meningkatnya kepuasan masyarakat" tanpa satuan | Gunakan "Indeks Kepuasan Masyarakat (skala 1-4)" |
| F05 | Nomenklatur tidak standar | Program/kegiatan tidak sesuai Kepmendagri 050-5889 | Sesuaikan dengan kodefikasi resmi |

### Kesalahan Umum (Perlu Diperbaiki)
| Kode | Kesalahan | Dampak |
|---|---|---|
| U01 | Terlalu banyak IKU per sasaran (>5) | Menyulitkan fokus dan pengukuran |
| U02 | Sasaran terlalu umum | Sulit diukur capaiannya |
| U03 | Analisis LKIP hanya naratif angka | Tidak menunjukkan akuntabilitas sejati |
| U04 | Target terlalu mudah (100% di tahun pertama) | Menunjukkan kurangnya ambisi/stretching |
| U05 | Tidak ada sumber data indikator | Validitas pengukuran diragukan |

---

## Format Laporan Review

Claude harus menyajikan hasil review dalam format berikut:

```
## LAPORAN REVIEW SAKIP
### [Jenis Dokumen] — [Nama OPD]
### Tanggal Review: [Tanggal]

---

### A. RINGKASAN PENILAIAN

| Aspek | Skor | Keterangan |
|---|---|---|
| Kelengkapan Struktur | [X/10] | ... |
| Kualitas Indikator | [X/10] | ... |
| Kualitas Target | [X/10] | ... |
| Konsistensi Internal | [X/10] | ... |
| **Total** | **[X/40]** | **[Kategori]** |

---

### B. TEMUAN UTAMA

**Kekuatan:**
1. ...
2. ...

**Kelemahan Kritis:**
1. [F-code] [Deskripsi masalah]
   → Rekomendasi: [Tindakan konkret]

**Kelemahan Minor:**
1. [U-code] [Deskripsi masalah]
   → Rekomendasi: [Tindakan konkret]

---

### C. REKOMENDASI PRIORITAS
[3–5 rekomendasi paling penting, diurutkan berdasarkan urgensi]
```
