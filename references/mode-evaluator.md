# Mode EVALUATOR — Simulasi Penilaian AKIP
## Berdasarkan PermenPAN-RB Nomor 88 Tahun 2021

---

## Komponen dan Bobot Penilaian AKIP

| No | Komponen | Bobot |
|---|---|---|
| 1 | Perencanaan Kinerja | 30% |
| 2 | Pengukuran Kinerja | 25% |
| 3 | Pelaporan Kinerja | 15% |
| 4 | Evaluasi Internal | 10% |
| 5 | Capaian Kinerja | 20% |
| | **TOTAL** | **100%** |

---

## Predikat Nilai AKIP

| Rentang Nilai | Predikat | Interpretasi |
|---|---|---|
| 90 – 100 | **AA** | Sangat Memuaskan |
| 80 – 89 | **A** | Memuaskan |
| 70 – 79 | **BB** | Sangat Baik |
| 60 – 69 | **B** | Baik |
| 50 – 59 | **CC** | Cukup (Perlu Perbaikan) |
| 30 – 49 | **C** | Kurang |
| 0 – 29 | **D** | Sangat Kurang |

---

## Rincian Komponen 1: Perencanaan Kinerja (30%)

### Sub-komponen
| Sub-komponen | Bobot |
|---|---|
| 1a. Rencana Strategis (Renstra) | 10% |
| 1b. Perencanaan Kinerja Tahunan (Renja + PK) | 20% |

### Kriteria Penilaian Renstra (1a)
| Aspek | Nilai Penuh | Indikator |
|---|---|---|
| Dokumen Renstra ada & ditetapkan secara formal | 2 | SK penetapan tersedia |
| Tujuan dan sasaran terukur | 2 | Ada IKU dengan satuan |
| Indikator kinerja tujuan bertipologi outcome/dampak | 2 | Tidak ada input/aktivitas |
| Target jangka menengah ditetapkan | 2 | Target per tahun tersedia |
| Selaras dengan RPJMD | 2 | Sasaran OPD mendukung sasaran RPJMD |

### Kriteria Penilaian Renja + PK (1b)
| Aspek | Nilai Penuh | Indikator |
|---|---|---|
| PK ditetapkan secara formal dan tepat waktu | 4 | Ditandatangani awal tahun |
| Sasaran PK selaras dengan Renstra | 4 | Konsistensi target tahunan |
| IKU dalam PK terukur dan relevan | 4 | SMART-C terpenuhi |
| Cascading PK tersedia (eselon II s/d IV) | 4 | Dokumen PK semua level |
| Program/anggaran dalam PK akurat | 4 | Sinkron dengan DPA |

---

## Rincian Komponen 2: Pengukuran Kinerja (25%)

### Sub-komponen
| Sub-komponen | Bobot |
|---|---|
| 2a. Pemenuhan Pengukuran | 5% |
| 2b. Kualitas Pengukuran | 12,5% |
| 2c. Implementasi Pengukuran | 7,5% |

### Kriteria Kunci
| Aspek | Nilai Penuh | Indikator |
|---|---|---|
| Seluruh IKU diukur capaiannya | 5 | Tidak ada IKU kosong |
| Terdapat mekanisme pengumpulan data | 5 | SOP/sistem pengumpulan data |
| Data pengukuran dapat diverifikasi | 5 | Sumber data jelas |
| Pengukuran dilakukan periodik (minimal triwulanan) | 5 | Ada laporan berkala |
| Pengukuran digunakan sebagai dasar keputusan | 5 | Ada bukti pemanfaatan |

---

## Rincian Komponen 3: Pelaporan Kinerja (15%)

### Sub-komponen
| Sub-komponen | Bobot |
|---|---|
| 3a. Pemenuhan Pelaporan | 3% |
| 3b. Kualitas Pelaporan | 7,5% |
| 3c. Pemanfaatan Informasi Kinerja | 4,5% |

### Kriteria Kunci
| Aspek | Nilai Penuh | Indikator |
|---|---|---|
| LKIP disusun dan disampaikan tepat waktu | 3 | Sebelum Maret tahun berikutnya |
| Menyajikan info capaian vs target | 3 | Ada tabel capaian lengkap |
| Analisis penyebab keberhasilan/kegagalan | 3 | Narasi analisis ada |
| Perbandingan dengan tahun sebelumnya | 3 | Ada data longitudinal |
| Informasi kinerja digunakan dalam perencanaan | 3 | Ada bukti pemanfaatan LKIP |

---

## Rincian Komponen 4: Evaluasi Internal (10%)

### Kriteria Kunci
| Aspek | Nilai Penuh | Indikator |
|---|---|---|
| Ada evaluasi akuntabilitas kinerja internal | 4 | Laporan evaluasi APIP |
| Rekomendasi evaluasi ditindaklanjuti | 3 | Bukti tindak lanjut |
| Pemantauan pencapaian kinerja berkala | 3 | Laporan monitoring triwulanan |

---

## Rincian Komponen 5: Capaian Kinerja (20%)

### Sub-komponen
| Sub-komponen | Bobot |
|---|---|
| 5a. Capaian Output | 5% |
| 5b. Capaian Outcome | 10% |
| 5c. Kinerja Lainnya | 5% |

### Formula Capaian Kinerja
```
Nilai Komponen 5 = (Rata-rata % Capaian IKU × Bobot) / 100

Kategori Capaian:
≥ 100% = 20 poin (nilai penuh)
85–99% = 17 poin
70–84% = 14 poin
55–69% = 11 poin
< 55%  = Sesuai proporsi
```

---

## Alur Simulasi Penilaian AKIP

### Input yang Diperlukan dari Pengguna
1. Dokumen Renstra OPD (atau rangkumannya)
2. Dokumen PK tahun yang dievaluasi
3. Dokumen LKIP/LAKIP
4. Laporan evaluasi internal (jika ada)
5. Data capaian IKU (realisasi vs target)

### Prosedur Simulasi

**Tahap 1: Penilaian Komponen 1 (Perencanaan)**
- Periksa keberadaan dan kualitas Renstra
- Periksa keberadaan dan kualitas PK (semua level)
- Hitung skor 1a dan 1b

**Tahap 2: Penilaian Komponen 2 (Pengukuran)**
- Periksa apakah semua IKU diukur
- Periksa kualitas mekanisme pengukuran
- Hitung skor 2a, 2b, 2c

**Tahap 3: Penilaian Komponen 3 (Pelaporan)**
- Periksa LKIP (ada/tidak, kualitas, ketepatan waktu)
- Hitung skor 3a, 3b, 3c

**Tahap 4: Penilaian Komponen 4 (Evaluasi)**
- Periksa keberadaan evaluasi internal
- Hitung skor komponen 4

**Tahap 5: Penilaian Komponen 5 (Capaian)**
- Hitung rata-rata capaian IKU outcome
- Konversi ke nilai komponen 5

**Tahap 6: Agregasi dan Predikat**
```
Total = (Skor1 × 30%) + (Skor2 × 25%) + (Skor3 × 15%)
        + (Skor4 × 10%) + (Skor5 × 20%)
```

---

## Format Output Simulasi Penilaian

```
## LEMBAR SIMULASI PENILAIAN AKIP
### [Nama OPD] — Tahun Evaluasi: [Tahun]
### *Catatan: Ini adalah simulasi internal, bukan hasil evaluasi resmi*

---

### RINGKASAN NILAI

| Komponen | Bobot | Nilai Mentah | Nilai Tertimbang |
|---|---|---|---|
| 1. Perencanaan Kinerja | 30% | [X]/100 | [X] |
| 2. Pengukuran Kinerja | 25% | [X]/100 | [X] |
| 3. Pelaporan Kinerja | 15% | [X]/100 | [X] |
| 4. Evaluasi Internal | 10% | [X]/100 | [X] |
| 5. Capaian Kinerja | 20% | [X]/100 | [X] |
| **TOTAL** | **100%** | | **[TOTAL]** |

**PREDIKAT: [AA/A/BB/B/CC/C/D]**
**Interpretasi: [Sangat Memuaskan/dst]**

---

### ANALISIS PER KOMPONEN

#### Komponen 1: Perencanaan Kinerja
**Nilai: [X]/30**

Kekuatan:
- ...

Kelemahan:
- ...

Rekomendasi:
- ...

[dst untuk setiap komponen]

---

### PRIORITAS PERBAIKAN UNTUK NAIK PREDIKAT

Untuk mencapai predikat [target predikat], OPD perlu meningkatkan:
1. [Komponen/aspek yang paling berpotensi ditingkatkan]
2. ...
3. ...
```
