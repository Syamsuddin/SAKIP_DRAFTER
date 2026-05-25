<!-- HEADER IMAGE-->
<p align="center">
  <img src="https://raw.githubusercontent.com/Syamsuddin/SAKIP_DRAFTER/main/references/sakip-drafter-header.png" alt="SAKIP Drafter Header" width="80%" />
</p>

<h1 align="center">SAKIP_DRAFTER</h1>
<p align="center">
  <b>Operasional Otomatisasi Dokumen SAKIP</b><br>
  <i>Konsultan Virtual SAKIP — Penyusunan, Review, Cascading, Indikator, & Evaluasi AKIP</i>
</p>

<p align="center">
  <!-- Badges: replace shields URLs with ones that match your repo/features -->
  <a href="https://github.com/Syamsuddin/SAKIP_DRAFTER/releases"><img src="https://img.shields.io/github/v/release/Syamsuddin/SAKIP_DRAFTER?label=release" alt="Latest Release"></a>
  <a href="https://github.com/Syamsuddin/SAKIP_DRAFTER/stargazers"><img src="https://img.shields.io/github/stars/Syamsuddin/SAKIP_DRAFTER?style=social" alt="GitHub Stars"></a>
  <a href="https://github.com/Syamsuddin/SAKIP_DRAFTER/actions/workflows/ci.yml"><img src="https://img.shields.io/github/workflow/status/Syamsuddin/SAKIP_DRAFTER/CI/main?label=build" alt="Build Status"></a>
  <img alt="Platform" src="https://img.shields.io/badge/platform-birokrasi%20Indonesia-blue.svg">
  <img alt="Regulasi" src="https://img.shields.io/badge/regulasi-Permendagri86%7CPerpres29-green">
  <img alt="Mode" src="https://img.shields.io/badge/mode-Drafter%2CReviewer%2CCascader%2CIndikator%2CEvaluator-important">
</p>

---

## 🚀 Gambaran

**SAKIP_DRAFTER** adalah _skill AI_ yang membekali Claude untuk membantu Pemerintah Daerah menyusun, mereview, serta mengelola dokumen SAKIP secara otomatis dan profesional, mulai dari RPJMD hingga LKIP. Bot ini berperan sebagai **konsultan SAKIP** yang paham regulasi, pola cascading indikator, hingga format birokrasi Indonesia.

---

## 📚 Hierarki Dokumen SAKIP

```
RPJMD (5 thn) ← Visi/Misi Kepala Daerah
  └── Renstra OPD (5 thn)
        └── Renja OPD (1 thn)
              └── PK Eselon II (1 thn)
                    └── PK Eselon III (1 thn)
                          └── PK Eselon IV (1 thn)
                                └── SKP ASN (1 thn)
```

- **Cascading logis**: Setiap level WAJIB punya IKU sebagai _turunan logis_ dari level sebelumnya.

---

## 🛠️ 5 Mode Operasi

| Mode       | Deskripsi | File Referensi |
|------------|-----------|----------------|
| **Drafter**    | Menyusun dokumen SAKIP dari nol           | [mode-drafter.md](references/mode-drafter.md) |
| **Reviewer**   | Menganalisis/merekomendasi perbaikan dokumen | [mode-reviewer.md](references/mode-reviewer.md) |
| **Cascader**   | Breakdown/cascading kinerja lintas level   | [mode-cascader.md](references/mode-cascader.md) |
| **Indikator**  | Merancang IKU/IKK “SMART-C” & tipologi     | [mode-indikator.md](references/mode-indikator.md) |
| **Evaluator**  | Simulasi penilaian AKIP PermenPAN 88/2021  | [mode-evaluator.md](references/mode-evaluator.md) |

---

## 🔍 Deteksi Mode Otomatis

| Kata Kunci                | Mode         |
|---------------------------|-------------|
| buatkan, susunkan, draftkan, tuliskan | Drafter    |
| review, nilai, cek, evaluasi dokumen   | Reviewer   |
| turunkan, cascading, breakdown jabatan | Cascader   |
| IKU, IKK, indikator, ukuran kinerja    | Indikator  |
| nilai AKIP, simulasi evaluasi          | Evaluator  |

---

## ✅ Prosedur Wajib Input

Sebelum generate dokumen, WAJIB menanyakan data berikut:

- **Nama OPD** & **Kabupaten/Kota**
- **Periode** (tahun/rentang)
- **Mode Output**: narasi / tabel / JSON / kombinasi

_Spesifik per dokumen: lihat file referensi mode terkait._

---

## 🎨 Format Output

- **Narasi**: Bahasa Indonesia formal sesuai PUEBI
- **Tabel (markdown)**: Header ringkas, checklist √, % 2 desimal
- **JSON**: Skema sesuai [json-schema.md](references/json-schema.md)

---

## 📖 Regulasi Utama

- **Perpres 29/2014** — SAKIP
- **Permendagri 86/2017** — RPJMD, Renstra, Renja
- **Kepmendagri 050-5889/2021** — Nomenklatur program/kegiatan
- **PermenPAN-RB 53/2014** — PK, LKIP
- **PermenPAN-RB 88/2021** — Penilaian AKIP
- **PermenPAN-RB 6/2022** — SKP & Manajemen ASN

[Lihat regulasi detail →](references/regulasi.md)

---

## 🧩 Tipologi Indikator (Ringkasan)

| Tipologi  | Level                    | Contoh                  |
|-----------|--------------------------|-------------------------|
| Dampak    | RPJMD/Renstra lintas OPD | IPM, Angka Kemiskinan   |
| Hasil     | Renstra OPD/PK Eselon II | % Layanan Terpenuhi     |
| Keluaran  | Renja/PK Eselon III–IV   | Jumlah Dokumen/Peserta  |
| Proses    | SKP ASN                  | Jumlah Laporan Dibuat   |
| Masukan   | Semua level              | Anggaran, SDM           |

:warning: **IKU tidak boleh tipologi input sebagai utama!**

---

## 🎯 Kualitas & Validasi Output

- [x] IKU/IKK SMART-C (spesifik, measurable, dst.)
- [x] Cascading logis
- [x] Nomenklatur sesuai Kepmendagri
- [x] Bukan indikator aktivitas “menyamar” IKU
- [x] Target berbasis baseline (jika ada)
- [x] Bahasa sesuai format birokrasi Indonesia

---

## 📬 Kontribusi & Lisensi

Kontribusi terbuka melalui PR/Github Issues.  
Lisensi: [MIT](LICENSE)
Penulis: syams_iders - NUSTEK AI

---

<p align="center"><i>Dokumentasi lengkap setiap mode, tipologi, dan template tersedia di folder <code>references/</code></i></p>
