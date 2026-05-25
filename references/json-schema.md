# JSON Schema — SAKIP_DRAFTER Output untuk Integrasi Sistem

Gunakan skema ini ketika pengguna meminta output JSON atau ketika output
akan diintegrasikan ke dalam aplikasi (DeDi, SIM, atau sistem lainnya).

---

## Schema 1: Renstra OPD

```json
{
  "renstra": {
    "metadata": {
      "nama_opd": "string",
      "kode_opd": "string",
      "kabupaten_kota": "string",
      "provinsi": "string",
      "periode_awal": "YYYY",
      "periode_akhir": "YYYY",
      "tanggal_penetapan": "YYYY-MM-DD",
      "nomor_sk": "string"
    },
    "tujuan": [
      {
        "id": "T.01",
        "rumusan": "string",
        "indikator": [
          {
            "id": "IT.01.01",
            "nama": "string",
            "satuan": "string",
            "tipologi": "dampak|outcome|output",
            "sumber_data": "string",
            "kondisi_awal": {
              "tahun": "YYYY",
              "nilai": "number|string"
            },
            "target": [
              {"tahun": "YYYY", "nilai": "number|string"}
            ],
            "kondisi_akhir": "number|string"
          }
        ],
        "sasaran": [
          {
            "id": "S.01.01",
            "rumusan": "string",
            "indikator": [
              {
                "id": "IK.01.01.01",
                "nama": "string",
                "satuan": "string",
                "tipologi": "outcome|output",
                "sumber_data": "string",
                "kondisi_awal": {
                  "tahun": "YYYY",
                  "nilai": "number|string"
                },
                "target": [
                  {"tahun": "YYYY", "nilai": "number|string"}
                ],
                "kondisi_akhir": "number|string"
              }
            ],
            "strategi": ["string"],
            "arah_kebijakan": ["string"],
            "program": [
              {
                "kode_program": "string",
                "nama_program": "string",
                "pagu_indikatif": [
                  {"tahun": "YYYY", "nilai": "number"}
                ]
              }
            ]
          }
        ]
      }
    ]
  }
}
```

---

## Schema 2: Perjanjian Kinerja (PK)

```json
{
  "perjanjian_kinerja": {
    "metadata": {
      "nama_opd": "string",
      "kabupaten_kota": "string",
      "tahun": "YYYY",
      "tanggal_pk": "YYYY-MM-DD"
    },
    "pihak_pertama": {
      "nama": "string",
      "nip": "string",
      "jabatan": "string",
      "eselon": "II|III|IV"
    },
    "pihak_kedua": {
      "nama": "string",
      "nip": "string",
      "jabatan": "string"
    },
    "sasaran_kinerja": [
      {
        "id": "SK.01",
        "rumusan_sasaran": "string",
        "indikator": [
          {
            "id": "IK.01.01",
            "nama": "string",
            "satuan": "string",
            "target": "number|string"
          }
        ]
      }
    ],
    "program_kegiatan": [
      {
        "kode": "string",
        "nama": "string",
        "anggaran": "number"
      }
    ],
    "total_anggaran": "number"
  }
}
```

---

## Schema 3: Capaian Kinerja / LKIP Summary

```json
{
  "capaian_kinerja": {
    "metadata": {
      "nama_opd": "string",
      "kabupaten_kota": "string",
      "tahun_pelaporan": "YYYY",
      "tanggal_laporan": "YYYY-MM-DD"
    },
    "ringkasan_eksekutif": "string",
    "sasaran": [
      {
        "id": "SK.01",
        "rumusan_sasaran": "string",
        "indikator": [
          {
            "id": "IK.01.01",
            "nama": "string",
            "satuan": "string",
            "target": "number|string",
            "realisasi": "number|string",
            "persentase_capaian": "number",
            "kategori": "Sangat Berhasil|Berhasil|Cukup Berhasil|Kurang Berhasil",
            "analisis": "string",
            "hambatan": ["string"],
            "upaya_tindak_lanjut": ["string"]
          }
        ],
        "rata_rata_capaian": "number",
        "kategori_sasaran": "string"
      }
    ],
    "realisasi_anggaran": [
      {
        "kode_program": "string",
        "nama_program": "string",
        "pagu": "number",
        "realisasi": "number",
        "persentase_serapan": "number"
      }
    ],
    "total_pagu": "number",
    "total_realisasi": "number",
    "total_serapan_persen": "number"
  }
}
```

---

## Schema 4: Matriks Cascading

```json
{
  "cascading": {
    "metadata": {
      "nama_opd": "string",
      "tahun": "YYYY",
      "tanggal_dibuat": "YYYY-MM-DD"
    },
    "level": [
      {
        "eselon": "II|III|IV",
        "nama_jabatan": "string",
        "nama_pejabat": "string",
        "sasaran": [
          {
            "id": "string",
            "rumusan": "string",
            "iku": [
              {
                "id": "string",
                "nama": "string",
                "satuan": "string",
                "target": "number|string",
                "tipologi": "outcome|output|sub-output",
                "mendukung_iku_atasan_id": "string|null"
              }
            ]
          }
        ]
      }
    ]
  }
}
```

---

## Schema 5: Hasil Simulasi Evaluasi AKIP

```json
{
  "simulasi_akip": {
    "metadata": {
      "nama_opd": "string",
      "kabupaten_kota": "string",
      "tahun_evaluasi": "YYYY",
      "tanggal_simulasi": "YYYY-MM-DD",
      "catatan": "Ini adalah simulasi internal, bukan penilaian resmi"
    },
    "komponen": [
      {
        "kode": "K1",
        "nama": "Perencanaan Kinerja",
        "bobot_persen": 30,
        "nilai_mentah": "number",
        "nilai_tertimbang": "number",
        "sub_komponen": [
          {
            "kode": "K1a",
            "nama": "Rencana Strategis",
            "bobot_persen": 10,
            "nilai": "number",
            "catatan": "string"
          }
        ],
        "kekuatan": ["string"],
        "kelemahan": ["string"],
        "rekomendasi": ["string"]
      }
    ],
    "total_nilai": "number",
    "predikat": "AA|A|BB|B|CC|C|D",
    "interpretasi": "string",
    "prioritas_perbaikan": ["string"]
  }
}
```

---

## Panduan Penggunaan JSON di Aplikasi

### Endpoint yang Disarankan (untuk DeDi/SIM)
```
POST /api/sakip/renstra        → Schema 1
POST /api/sakip/pk             → Schema 2
POST /api/sakip/capaian        → Schema 3
POST /api/sakip/cascading      → Schema 4
POST /api/sakip/evaluasi       → Schema 5
```

### Catatan Implementasi
- Semua nilai moneter (anggaran) dalam satuan **Rupiah penuh** (integer)
- Persentase capaian menggunakan nilai **float** (misal: 87.50)
- Tanggal menggunakan format **ISO 8601** (YYYY-MM-DD)
- ID dokumen menggunakan format hierarkis (T.01, S.01.01, IK.01.01.01)
- Field `null` diizinkan untuk data yang belum tersedia
