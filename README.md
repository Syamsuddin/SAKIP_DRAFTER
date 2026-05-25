# SAKIP_DRAFTER Skill

**Asisten Perencana SAKIP untuk Pemerintah Daerah**

Skill ini membekali Claude dengan kemampuan menyusun, mereview, dan mensimulasikan
seluruh dokumen SAKIP (Sistem Akuntabilitas Kinerja Instansi Pemerintah) untuk
lingkungan Pemerintah Daerah — mulai RPJMD hingga LKIP/LAKIP.

---

## Fitur Utama

| Mode | Fungsi |
|---|---|
| **DRAFTER** | Menyusun draf dokumen SAKIP dari nol (Renstra, Renja, PK, LKIP, dll.) |
| **REVIEWER** | Menganalisis dan memberikan rekomendasi perbaikan dokumen |
| **CASCADER** | Menurunkan kinerja antar level eselon secara logis |
| **INDIKATOR** | Merancang IKU/IKK yang memenuhi kriteria SMART-C |
| **EVALUATOR** | Mensimulasikan penilaian AKIP (PermenPAN-RB 88/2021) |

Output tersedia dalam format **narasi birokrasi Indonesia**, **tabel Markdown**,
dan **JSON** untuk integrasi sistem.

---

## Dokumen yang Didukung

- RPJMD, Renstra OPD, Renja OPD
- Perjanjian Kinerja (PK) semua eselon
- IKU / IKK
- LKIP / LAKIP
- Pohon Kinerja & Matriks Cascading
- RKT (Rencana Kinerja Tahunan)

---

## Cara Install

### Jalur 1 — Claude.ai (Browser/Mobile) — Cara Termudah

Tidak memerlukan instalasi teknis. Cukup gunakan fitur **Projects** di claude.ai.

**Langkah-langkah:**

1. Buka [claude.ai](https://claude.ai) dan login
2. Klik menu **Projects** → **New Project**
3. Beri nama project, contoh: *"SAKIP Assistant Pemda"*
4. Klik tab **Project Instructions**
5. Buka file `SKILL.md` dari paket ini, **copy seluruh isinya**
6. Paste ke kolom Project Instructions → klik **Save**
7. Mulai chat baru dalam project tersebut

> Setiap anggota tim yang diundang ke project yang sama akan otomatis
> mendapatkan kemampuan SAKIP_DRAFTER tanpa perlu setup ulang.

**Alternatif (tanpa Project):**

Paste isi `SKILL.md` sebagai pesan pertama di chat baru:
```
Gunakan panduan berikut untuk setiap responsmu: [paste isi SKILL.md di sini]
```

---

### Jalur 2 — Claude Code (CLI) — Cara Resmi

Untuk pengguna Claude Code di terminal/VSCode/JetBrains.

**Prasyarat:** Claude Code sudah terinstall
```bash
npm install -g @anthropic-ai/claude-code
```

**Langkah instalasi:**

```bash
# 1. Buat folder skills jika belum ada
mkdir -p ~/.claude/skills

# 2. Copy file .skill ke folder tersebut
cp sakip-drafter.skill ~/.claude/skills/

# 3. Ekstrak file .skill (format ZIP)
cd ~/.claude/skills/
unzip sakip-drafter.skill -d sakip-drafter/

# 4. Verifikasi struktur hasil ekstrak
ls ~/.claude/skills/sakip-drafter/
# Seharusnya tampil: SKILL.md  references/  README.md
```

Setelah instalasi, Claude Code akan otomatis mendeteksi dan menggunakan skill
ini setiap kali Anda menyebut kata kunci SAKIP dalam percakapan.

**Lokasi folder skills per sistem operasi:**

| OS | Path |
|---|---|
| macOS / Linux | `~/.claude/skills/` |
| Windows | `C:\Users\[nama_user]\.claude\skills\` |

---

### Jalur 3 — Integrasi Aplikasi via API

Untuk developer yang ingin mengintegrasikan kemampuan SAKIP_DRAFTER ke dalam
aplikasi web (seperti DeDi, SIM, atau portal pemerintah).

**PHP (Laravel / Native):**

```php
<?php
// Load SKILL.md sebagai system prompt
$systemPrompt = file_get_contents(__DIR__ . '/sakip-drafter/SKILL.md');

$client = new \GuzzleHttp\Client();
$response = $client->post('https://api.anthropic.com/v1/messages', [
    'headers' => [
        'x-api-key'         => env('ANTHROPIC_API_KEY'),
        'anthropic-version' => '2023-06-01',
        'Content-Type'      => 'application/json',
    ],
    'json' => [
        'model'      => 'claude-sonnet-4-20250514',
        'max_tokens' => 4096,
        'system'     => $systemPrompt,
        'messages'   => [
            ['role' => 'user', 'content' => $userInput]
        ],
    ],
]);

$data = json_decode($response->getBody(), true);
echo $data['content'][0]['text'];
```

**JavaScript / Node.js:**

```javascript
import Anthropic from '@anthropic-ai/sdk';
import fs from 'fs';

const client = new Anthropic({ apiKey: process.env.ANTHROPIC_API_KEY });
const systemPrompt = fs.readFileSync('./sakip-drafter/SKILL.md', 'utf-8');

const response = await client.messages.create({
  model: 'claude-sonnet-4-20250514',
  max_tokens: 4096,
  system: systemPrompt,
  messages: [{ role: 'user', content: userInput }],
});

console.log(response.content[0].text);
```

**Python:**

```python
import anthropic

with open('./sakip-drafter/SKILL.md', 'r') as f:
    system_prompt = f.read()

client = anthropic.Anthropic(api_key="ANTHROPIC_API_KEY")
message = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=4096,
    system=system_prompt,
    messages=[{"role": "user", "content": user_input}]
)
print(message.content[0].text)
```

> **Catatan:** Untuk output JSON (integrasi database), minta pengguna
> menambahkan frasa *"dalam format JSON"* di akhir permintaan, atau
> hardcode instruksi tersebut di system prompt tambahan.

---

## Cara Berbagi ke Rekan Kerja

File `sakip-drafter.skill` dapat dibagikan melalui media apa pun:

```
📦 sakip-drafter.skill (±19KB)

Kirim via:
├── WhatsApp / Telegram
├── Email attachment
├── Google Drive / OneDrive
├── USB / Flashdisk
└── GitHub / GitLab (untuk tim developer)
```

Penerima cukup mengikuti salah satu jalur instalasi di atas sesuai
kebutuhannya masing-masing.

---

## Ringkasan Pemilihan Jalur

| Konteks Pengguna | Jalur yang Disarankan |
|---|---|
| Staf OPD / perencana, pakai browser | **Jalur 1** — Project Instructions claude.ai |
| Developer, pakai Claude Code CLI | **Jalur 2** — Install `.skill` file |
| Aplikasi web pemerintah (DeDi, SIM) | **Jalur 3** — Integrasi API |
| Berbagi ke banyak orang sekaligus | Kirim file `.skill` + arahkan ke README ini |

---

## Contoh Prompt Penggunaan

```
# Mode DRAFTER
"Buatkan draf Renstra Dinas Kesehatan Kabupaten Barito Utara 2025–2029.
 Visi Bupati: '...' Sasaran RPJMD yang relevan: ..."

# Mode REVIEWER
"Review IKU berikut dari Dinas Perhubungan, apakah sudah sesuai standar SAKIP:
 1. Jumlah rapat koordinasi = 12 kali
 2. Terlaksananya pengadaan rambu lalu lintas"

# Mode CASCADER
"Turunkan IKU Kepala Dinas Sosial berikut ke 3 Kabid di bawahnya."

# Mode INDIKATOR
"Bantu saya merancang IKU yang SMART untuk Dinas Lingkungan Hidup."

# Mode EVALUATOR
"Simulasikan nilai AKIP Dinas Pertanian kami dengan kondisi berikut: ..."

# Output JSON (untuk integrasi sistem)
"Buatkan Perjanjian Kinerja Dinas Pendidikan tahun 2025 dalam format JSON."
```

---

## Regulasi Referensi

| Regulasi | Substansi |
|---|---|
| Perpres 29/2014 | Landasan hukum SAKIP |
| Permendagri 86/2017 | Format RPJMD, Renstra, Renja |
| Kepmendagri 050-5889/2021 | Nomenklatur program/kegiatan |
| PermenPAN-RB 53/2014 | Format PK dan LKIP |
| PermenPAN-RB 88/2021 | Pedoman evaluasi AKIP |
| PermenPAN-RB 6/2022 | SKP dan kinerja ASN |

---

## Struktur File

```
sakip-drafter/
├── SKILL.md                           ← Inti skill (wajib untuk semua jalur)
├── README.md                          ← Panduan ini
└── references/
    ├── mode-drafter.md                ← Template 9 dokumen SAKIP
    ├── mode-reviewer.md               ← Checklist review & red flags
    ├── mode-cascader-indikator.md     ← Logika cascading & bank IKU
    ├── mode-evaluator.md              ← Komponen penilaian AKIP
    ├── json-schema.md                 ← 5 skema JSON untuk integrasi sistem
    └── regulasi.md                    ← Referensi regulasi & pasal kritis
```

---

## Dikembangkan Oleh
syams_ideris
**PT Nusa Smart Teknologi (NST/NUSTEK)**
Kalimantan Selatan, Indonesia

*Skill ini merupakan bagian dari ekosistem eGovernment NST untuk mendukung
penguatan akuntabilitas kinerja pemerintah daerah di Indonesia.*
