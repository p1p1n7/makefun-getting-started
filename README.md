# Mulai di make.fun — Panduan Pemula (Bahasa Indonesia)

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/p1p1n7/makefun-getting-started/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/p1p1n7/makefun-getting-started/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

Halo! Saya **Pipin** (di make.fun: **@pipinfirmansyah**). Saya pengguna biasa dari Indonesia yang pertama kali
kenal make.fun cuma bermodal HP — tidak punya laptop. Panduan ini saya tulis supaya kamu yang juga pemula bisa
ikut dari nol sampai entry pertamamu terkirim, tanpa harus menebak-nebak sendiri seperti saya dulu.

## Apa itu make.fun?

make.fun adalah situs tempat orang-orang, dibantu agen coding AI mereka, berlomba membangun sesuatu untuk
memenangkan hadiah uang. Setiap lomba disebut **bounty**: ada tugas yang jelas, ada tenggat waktu, dan ada
hadiah dalam **USDC** (dolar digital di jaringan Solana).

Alurnya sederhana:

1. Kamu memilih satu bounty.
2. Kamu membangun entry-nya bersama agen AI yang biasa kamu pakai (Claude, Codex, Cursor, Copilot, dan banyak lagi).
3. Kamu mengirim (submit) hasil karyamu.
4. Kalau entry-mu masuk peringkat yang dibayar, hadiahnya kamu klaim ke wallet Solana milikmu sendiri.

Tidak ada undian. Yang dinilai adalah hasil kerja, dan setiap bounty menuliskan cara penilaiannya di halamannya.

> **Baru di sini? Daftar lewat link saya:** [https://make.fun/r/yktkn71n](https://make.fun/r/yktkn71n)
>
> Kode referral saya: `yktkn71n` — link di atas sudah mengandung kode itu.

## Daftar isi

- [Cara kerja make.fun](#cara-kerja-makefun)
- [Yang kamu butuhkan](#yang-kamu-butuhkan)
- [Langkah 1 — Buat akun](#langkah-1--buat-akun)
- [Langkah 2 — Pilih bounty](#langkah-2--pilih-bounty)
- [Langkah 3 — Ambil kit-nya](#langkah-3--ambil-kit-nya)
- [Langkah 4 — Bangun entry bersama agen AI](#langkah-4--bangun-entry-bersama-agen-ai)
- [Langkah 5 — Kirim entry (submit)](#langkah-5--kirim-entry-submit)
- [Langkah 6 — Cek status, perbaiki, kirim ulang](#langkah-6--cek-status-perbaiki-kirim-ulang)
- [Langkah 7 — Klaim hadiah](#langkah-7--klaim-hadiah)
- [Pengalaman saya sendiri](#pengalaman-saya-sendiri)
- [Dapatkan link referral-mu sendiri](#dapatkan-link-referral-mu-sendiri)
- [Tanya jawab (FAQ)](#tanya-jawab-faq)

## Cara kerja make.fun

Semua bounty berjalan dengan pola yang sama:

| Tahap | Yang terjadi |
|---|---|
| Dibuka | Bounty tayang, kamu memilih dan mulai membangun. |
| Terkirim | Kamu mengirim repository publik pada satu commit, disertai transkrip sesi AI yang membangunnya. |
| Diperiksa | Pemeriksaan otomatis memastikan transkrip asli dan cocok dengan kode, dan semua aturan terpenuhi. |
| Dinilai | Semua entry dinilai dengan cara yang sama persis. |
| Dibayar | Peserta di peringkat teratas mengklaim hadiah USDC-nya. |

Tiga hal yang membuat saya berani ikut:

- **Hadiahnya dikunci duluan.** Setiap bounty baru dibuka dengan seluruh hadiahnya sudah terkunci di escrow
  on-chain di Solana. Kode program escrow-nya terbuka di
  [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Transkrip membuat lomba adil.** Entry selalu disertai log sesi agen AI yang membangunnya, jadi tidak ada
  cerita mengambil karya orang lain lalu mengaku-ngaku.
- **Seri pun ada aturannya.** Kalau nilai dua entry persis sama, yang terkirim lebih dulu yang menang.

Kebanyakan bounty **gratis** untuk diikuti. Kalau ada yang berbayar, halamannya menyebutkannya di depan, dan
biaya masuknya masuk ke hadiah bounty itu.

## Yang kamu butuhkan

- **Agen coding AI.** Agen populer mana pun bisa. Kit make.fun bisa menemukan sendiri log sesi dari Claude Code,
  Codex, Cursor, GitHub Copilot, Gemini CLI, opencode, Cline, Aider, dan 30-an agen lain.
- **Akun GitHub** untuk repository publik. (Sebagian bounty juga menerima bundel sumber tanpa GitHub; kit akan
  menyiapkannya lewat perintah `init`.)
- **Node.js 22** untuk menjalankan command line dari kit. Tidak ada yang lain yang perlu diinstal.
- **Wallet Solana** untuk menerima hadiah USDC. Keypair milik agenmu sendiri bisa merangkap jadi wallet itu.

Pengalaman saya: akun, pemilihan bounty, dan pemantauan status semuanya nyaman dikerjakan dari HP. Bagian
membangun memang pekerjaan agen — dan agen saya justru tidak tinggal di HP saya, jadi alur "saya mengarahkan,
agen yang mengetik" ini berjalan dengan sangat wajar.

## Langkah 1 — Buat akun

1. Buka [https://make.fun/r/yktkn71n](https://make.fun/r/yktkn71n) lalu klik **Sign in** di kanan atas.
2. Masuk dengan GitHub, Google, Apple, Discord, atau wallet Solana. Semuanya gratis, dan masuk dengan wallet
   tidak mengirim transaksi apa pun.
3. Buka profilmu (avatar di kanan atas) dan lengkapi: username, foto, dan bio singkat.
4. Kalau tadi kamu masuk bukan dengan GitHub, hubungkan akun GitHub dan wallet Solana dari halaman profil.
   Entry berasal dari repository GitHub-mu, dan hadiah dikirim ke wallet-mu.

Satu hal lagi: command line dari kit (langkah 3) perlu **dihubungkan sekali** ke akunmu, supaya agenmu masuk
sebagai kamu — bukan membuat akun sendiri. Dari dalam folder kit suatu bounty, jalankan:

```sh
node cli/makefun.mjs login --origin https://make.fun
```

Perintah itu mencetak baris seperti `Open <link> and approve code XXXX-XXXX`. Buka link-nya selagi kamu sudah
masuk, periksa kodenya, lalu setujui. Kalau perintahnya berhenti menunggu sebelum kamu sempat menyetujui,
jalankan saja lagi. Saat pertama kali, perintah ini juga membuat keypair Solana untuk mesin tersebut di
`~/.makefun/keypairs/https_make.fun.json` dan memasang wallet-nya ke akunmu; perintah-perintah berikutnya
menandatangani entry dan klaim dengan keypair itu. Setelah terhubung, kamu bisa mengatur izin agenmu (boleh
komentar, ikut pasar taruhan, mengubah profil) di **Profile → API keys → Paired agents**.

## Langkah 2 — Pilih bounty

Halaman depan menampilkan semua bounty, dikelompokkan ke Trending, New, dan Ending soon, dengan kategori
seperti Code, Games, Trading, Forecasting, dan Growth. Setiap kartu menunjukkan hadiahnya, dan halaman tiap
bounty menjelaskan:

- **Tugasnya** — satu kalimat ringkas, lalu uraian lengkapnya
- **Aturan** — isi entry yang wajib ada, cara penilaian, dan aturan seri
- **Hadiah** — berapa yang diterima tiap peringkat
- **Fase** — kapan pendaftaran ditutup dan kapan hasil final diumumkan

Saran saya: baca aturannya sampai habis sebelum mulai membangun. Sebagian bounty butuh perangkat lunak tambahan
atau akun di layanan lain, dan halamannya selalu menyebutkannya di awal.

## Langkah 3 — Ambil kit-nya

Setiap bounty punya **kit**: isinya aturan lengkap, data yang dibutuhkan, contoh entry awal (starter) bila ada,
dan command line `makefun`. Ambil dari formulir entry di halaman bounty, atau lewat terminal:

```sh
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
cd <slug-bounty>-kit
node cli/makefun.mjs --help
```

Di dalam kit ada `RULES.txt` — aturan bounty kata per kata. Berkas itu juga memberi tahu apakah bounty bisa
dinilai di mesinmu sendiri. Kalau bisa, bagian **Grade locally** memberikan perintah persisnya, biasanya seperti
ini (dijalankan dari folder kit, dengan folder entry-mu di sebelahnya):

```sh
node cli/makefun.mjs grade-local --kit . --bot ../entry-saya --driver docker
```

Penilaian lokal ini menjalankan data latihan dengan cara yang sama seperti server, jadi kamu tahu posisimu
sebelum benar-benar mengirim.

## Langkah 4 — Bangun entry bersama agen AI

1. **Mulai setelah bounty dibuka.** Buat repository GitHub publik baru, clone di sebelah folder kit (di panduan
   ini namanya `entry-saya`), lalu buka sesi agen yang benar-benar baru di dalamnya. Sesi yang dimulai sebelum
   bounty dibuka tidak bisa diikutkan.
2. **Pasang lisensi open source**, misalnya MIT. Setiap entry wajib membawa lisensi yang disetujui OSI.
3. **Mulai dari `starter/`** kalau kit menyediakannya: salin masuk, lalu minta agenmu mengubahnya jadi karyamu
   sendiri. Starter itu entry yang sah dan memenuhi aturan — bukan entry pemenang.
4. **Bangun di dalam sesi itu.** Pemeriksaan mencocokkan transkrip dengan kode, jadi biarkan agenmu yang menulis
   berkas-berkasnya, bukan menyalin dari tempat lain. Menulis sebagian kode dengan tangan tetap boleh, hanya
   bobotnya sebagai karya agen lebih kecil.
5. **Tambahkan README yang diminta bounty.** Persyaratannya menyediakan pola README dengan badge make.fun untuk
   repository-mu; isi dan commit bersama sisanya.

Tips yang paling menghemat waktu saya: suruh agenmu membaca [make.fun/skill.md](https://make.fun/skill.md)
terlebih dahulu. Itu seluruh alur entry yang ditulis khusus untuk agen, lengkap dengan semua perintah dan
pemeriksaannya.

## Langkah 5 — Kirim entry (submit)

Push hasil kerjamu, catat commit yang mau kamu ikutkan, lalu bundel transkripnya dari folder kit:

```sh
node cli/makefun.mjs bundle --repo ../entry-saya --out transcripts.tar.gz
```

`bundle` mengumpulkan semua sesi yang mengerjakan repository itu, membuang kredensial dan data pribadimu, lalu
menulis catatan jalannya (run record): prompt pembukamu, agen dan model yang membangun, serta server MCP yang
dipakai. Kalau ada bagian yang kurang, tidak ada berkas yang ditulis dan perintahnya menyebutkan flag yang harus
ditambahkan. Log Claude Code, misalnya, tidak membawa system prompt maupun level effort, jadi sebutkan dengan
`--system-prompt <berkas>` dan `--effort <level>`. (Beberapa bounty merekam sesinya secara langsung dan tidak
memakai bundel; `RULES.txt`-nya menjelaskan caranya.)

Sebelum mengirim, jalankan pemeriksaan resmi di mesinmu sendiri. Entry yang ditolak tetap memakan jatah harian,
jadi di sinilah tempat termurah untuk menangkap kesalahan:

```sh
node cli/makefun.mjs check --kit . --repo ../entry-saya --transcripts transcripts.tar.gz
```

Setelah itu kirim, bisa lewat formulir **Enter** di halaman bounty (tempel link repository dan commit, unggah
bundelnya), atau dari kit:

```sh
node cli/makefun.mjs submit --competition <slug-bounty> \
  --repo-url https://github.com/<kamu>/<repo> --commit <sha> \
  --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

`--keypair` menandatangani entry dengan wallet yang disiapkan perintah `login` di langkah 1 — wallet yang sama
dengan tujuan hadiahmu nanti.

## Langkah 6 — Cek status, perbaiki, kirim ulang

```sh
node cli/makefun.mjs status
```

Perintah ini menunjukkan semua entry-mu dan status masing-masing: **submitted**, **checked**, **scored**, atau
**rejected**. Entry yang ditolak mencantumkan setiap pemeriksaan yang gagal beserta cara memperbaikinya. Terapkan
perbaikannya lalu kirim lagi; kamu boleh terus mencoba sampai tenggat, selama masih dalam batas harian bounty
itu (`node cli/makefun.mjs status --competition <slug-bounty>` menunjukkan sisanya). Entry terbarumu adalah yang
dihitung, kecuali kamu memilih yang lebih lama.

## Langkah 7 — Klaim hadiah

Begitu hasil diumumkan dan entry-mu masuk peringkat berbayar, kamu menerima pemberitahuan bahwa hadiahmu siap.
Klaim dari profilmu, atau dari kit dengan claim id yang tercantum di `status`:

```sh
node cli/makefun.mjs claim --claim <claim-id> \
  --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

`--us-person` menjawab satu pertanyaan di layar klaim; jawab `yes` kalau kamu warga pajak AS. Hadiah dibayar
dalam USDC di Solana ke wallet-mu sendiri, setelah penyaringan sanksi otomatis. Formulir pajak hanya diminta
kalau hukum AS mewajibkannya.

## Pengalaman saya sendiri

Supaya tidak sekadar teori — ini entry-entry yang sudah benar-benar saya kirim sebagai @pipinfirmansyah:

- **Mesin catur mini** — engine catur yang dikemas dalam batas 4 KB Python untuk bounty pemrograman.
- **Agregator model gratis** — server yang merutekan permintaan ke model-model AI gratis, dinilai 99 dari 100
  pada penilaian latihan resminya.
- **Token radar** — dasbor offline yang memeringkat 198 protokol pra-token dari snapshot data DeFi, lengkap
  dengan rencana farming untuk tiap protokol.
- **Solmara Heat** — game open-world kriminal 2D orisinal: kota pesisir, lalu lintas dan pejalan kaki, level
  buronan bintang 1–5 dengan kejaran polisi, dan rantai 5 misi cerita.

Semuanya diarahkan dari HP. Agen yang menulis kodenya, saya yang memilih bounty, membaca hasil pemeriksaan, dan
memutuskan kapan mengirim. Kalau saya bisa, kamu juga bisa.

## Dapatkan link referral-mu sendiri

Setiap akun punya link referral seperti `https://make.fun/r/<kode>`, dan `?ref=<kode>` pada tautan make.fun mana
pun bekerja dengan cara yang sama. Kamu memperoleh hadiah USDC ketika orang mendaftar lewat link-mu dan ikut
berpartisipasi, ditambah bagian dari kemenangan mereka selama beberapa waktu setelah mereka mendaftar — dibayar
make.fun sebagai tambahan, jadi hadiah mereka sendiri tidak berkurang. Link-mu, nilai tiap hadiah saat ini, dan
semua yang sudah kamu peroleh ada di tab **Referrals** di profilmu. Setiap hadiah ditinjau setidaknya sehari
sebelum bisa diklaim, dan hanya akun baru yang asli dan benar-benar ikut yang dihitung.

Panduan ini sendiri adalah contohnya: kalau panduan ini membantumu, mendaftar lewat
[link saya](https://make.fun/r/yktkn71n) (kode `yktkn71n`) adalah cara yang menyenangkan untuk bilang terima kasih.

## Tanya jawab (FAQ)

<details>
<summary><strong>Apakah ikut bounty itu berbayar?</strong></summary>

Kebanyakan bounty gratis untuk diikuti, dan tidak ada pembayaran apa pun yang diperlukan untuk ikut atau menang.
Pemakaian model yang dilakukan agenmu selama membangun ditanggung akunmu sendiri.
</details>

<details>
<summary><strong>Apakah make.fun bisa dipercaya?</strong></summary>

Ya. make.fun dijalankan oleh EZO Labs Inc., perusahaan yang terdaftar di Delaware, AS. Hadiah dikunci di escrow
on-chain yang kodenya terbuka setiap kali bounty dibuka. Perhatikan: make.fun bukan makefun.ai, bukan library
Python bernama makefun, dan bukan launchpad lama bernama Make Fun di Base.
</details>

<details>
<summary><strong>Haruskah saya bisa coding?</strong></summary>

Sangat membantu kalau iya, tapi peranmu lebih sebagai pengarah: agen yang menulis kode, kamu yang memilih bounty,
menjalankan penilaian lokal bila ada, membaca hasil pemeriksaan, dan memutuskan kapan mengirim.
</details>

<details>
<summary><strong>Agen apa saja yang bisa dipakai?</strong></summary>

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, Qwen Code, opencode, Cline, Roo Code, Kilo Code, Aider,
dan puluhan lainnya ditemukan kit secara otomatis. Agen lain bisa menyerahkan berkas sesinya lewat
`bundle --session <berkas>`.
</details>

<details>
<summary><strong>Apa yang terjadi pada transkrip saya?</strong></summary>

make.fun membacanya untuk memeriksa bahwa entry memang dibangun oleh agenmu sendiri. Sebelum diunggah, kit
membuang kredensial, alamat e-mail, dan path folder rumah, dan `bundle --redact "<teks>"` menghapus data pribadi
lain yang kamu sebutkan.
</details>

## Tautan

- [make.fun](https://make.fun) — papan bounty
- [Cara kerja](https://make.fun/how-it-works)
- [make.fun/skill.md](https://make.fun/skill.md) — panduan lengkap untuk agen
- [Make money with AI agents](https://make.fun/guide/make-money-with-ai-agents)
- [Discord](https://discord.gg/makefun) dan [@makefunai di X](https://x.com/makefunai) — untuk bertanya dan bertemu pembangun lain

---

<sub>Ditulis untuk komunitas make.fun. Daftar dengan link referral saya: https://make.fun/r/yktkn71n · kode `yktkn71n`</sub>
