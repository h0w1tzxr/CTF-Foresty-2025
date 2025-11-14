<div align="center">

<div align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZyPzorKkQfJFLlR7fuzNEKp3lCXvE3s5-9Q&s" height="200" alt="Logo Foresty Lab">
  
  <br><br>

  <img src="https://img.shields.io/badge/CTF%20Foresty%202025-Write_Up%20Hub-0f172a?style=for-the-badge&logo=github" alt="CTF Foresty Badge">
</div>

# 🌲 CTF Foresty 2025 — constantine
**Dokumentasi progress CTF buat belajar lagi, ada navigasi instan sama highlight.**

**CTF dan Write-Up dibantu oleh:**

[Google Gemini 2.5 Pro](https://gemini.google.com) · [ChatGPT 5.1 Extended Thinking](https://chatgpt.com/) · [Grok 4 Thinking](https://grok.com/)

</div>

---

## 🗺️ Map of Write-Ups
| Kategori | Gambaran | Status | CTA |
| --- | --- | --- | --- |
| **Binary Exploitation** |`Baby Pwn` `Karbit Checker` `Pemanasan-1` | 3 PDF | [Buka Folder](Binary%20Exploitation/)
| **Cryptography** |`RSA Shared Prime` `Operation Foresty` | 2 PDF | [Buka Folder](Cryptography/)
| **OSINT** |`Atmin Lagi` `Atmint` `Serlok` `Thr34t_4ct0r` | 4 PDF | [Buka Folder](OSINT/)
| **Forensic** |`Sound` `Meta` `Secretfile` | 5 PDF | [Buka Folder](Forensic/)
| **Reverse Engineering** |`Baby-Reveng` `Byte-Circus` `Ini Challenge Reverse?` | 3 PDF | [Buka Folder](Reverse%20Engineering/)
| **Web Exploit** |`Injection` `Restricted Area` `Toko Bendera` `iHGracias` | 4 PDF | [Buka Folder](Web%20Exploit/)
| **Misc** | `Tes Kejiwaan` `Soal UTBK` `Library in The Backrooms` | 3 PDF | [Buka Folder](Misc/)
| **Total** | | 24 |
> **Tip:** Tinggal klik apa yang mau kalian buka dan baca aja, simpel wok.

---

## 📚 Detail per Kategori
Pencet _accordion/panah_ di bawah buat ngebaca ringkasan tanpa ninggalin halaman.

<details>
<summary><b>🪓 Binary Exploitation</b></summary>

- `Baby Pwn.pdf`  Stack Buffer Overflow (Variable Overwrite). Mengeksploitasi input tanpa batas untuk menimpa variabel lokal atau return address tanpa proteksi Canary.
- `Karbit Checker.pdf`  Ret2Win via Buffer Overflow. Memanfaatkan fungsi gets() untuk menimpa Return Address (RIP) ke fungsi.
- `pemanasan-1.pdf`  Ret2Win & Stack Alignment. Teknik overflow untuk lompat ke fungsi win, namun memerlukan gadget RET kosong untuk memperbaiki stack alignment.

</details>

<details>
<summary><b>🔐 Cryptography</b></summary>

- `Operation Foresty.pdf`  Multi-layer Classical Cipher. Decoding bertingkat yang melibatkan Columnar Transposition, Hill, Affine, Vigenère, Substitution, dan ROT13.
- `RSA Shared Prime.pdf`  Common Factor Attack. Menyerang dua public key yang berbagi satu faktor prima (p) yang sama untuk memfaktorkan modulus (n).

</details>

<details>
<summary><b>🕵️ OSINT</b></summary>

- `Atmin Lagi.pdf`, `Atmint.pdf`  Geolocation (IMINT). Menentukan lokasi presisi menggunakan landmark visual (Masjid Bandara & Interior Terminal), disubmit dalam bentuk Google Plus Code.
- `Serlok.pdf`  Visual Reconnaissance. Mengidentifikasi lokasi Billard hanya dari teks samar pada latar belakang foto agar si bro bisa main billiard dan tidak jadi nolep.
- `Thr34t_4ct0r.pdf`  Threat Actor Profiling. Melacak identitas asli pelaku kebocoran data menggunakan BF Database Lookup ([bf.based.re](https://bf.based.re)).

</details>

<details>
<summary><b>🧪 Forensic</b></summary>

- `Sound.pdf`  Audio Spectrum Analysis. Menganalisis visual waveform audio untuk menemukan sandi Morse tersembunyi.
- `Meta.pdf`  Office XML Forensics. Menemukan hidden comment di dalam struktur XML .docx untuk mendapatkan password arsip ZIP bersarang.
- `Secretfile.pdf`  Recursive Archive Extraction. Otomatisasi ekstraksi file ZIP bertingkat (Matryoshka) menggunakan scripting via Python.
- `Cropped Top.pdf`  PNG Header Repair. Memperbaiki chunk IHDR (height) yang dimanipulasi agar gambar penuh dapat ditampilkan kembali.
- `Tutut.pdf`  Multi-stage Forensics. Kombinasi analisis audio (Morse ke URL) dan ekstraksi metadata gambar (Exiftool).

</details>

<details>
<summary><b>🧩 Reverse Engineering</b></summary>

- `Baby-Reveng.pdf`  Static Analysis & Deobfuscation. Menganalisis stack strings di Ghidra dan membuat solver untuk membalikkan logika penjumlahan array.
- `Byte-Circus.pdf`  Python Bytecode Decompilation. Mengembalikan file .pyc ke .py dan membalikkan logika XOR sederhana.
- `Ini Challenge Reverse_.pdf`  Basic Static Analysis. Pengambilan flag secara langsung menggunakan command `strings`.

</details>

<details>
<summary><b>🌐 Web Exploit</b></summary>

- `Injection.pdf`  SQL Injection & Command Injection. Auth bypass via SQLi dan eksekusi perintah OS (RCE) melalui fitur ping yang tidak disanitasi.
- `Restricted Area.pdf`  Source Code Review. Menemukan flag yang tersimpan dalam atribut value pada elemen HTML input yang tersembunyi.
- `Toko Bendera.pdf`  Dompdf RCE. Eksekusi kode jarak jauh dengan menyuntikkan font PHP berbahaya melalui kerentanan font caching di library Dompdf.
- `iHGracias.pdf`  Privilege Escalation & IDOR. Manipulasi cookie untuk menjadi admin dan mengakses data user lain (IDOR).

</details>

<details> <summary><b>📂 Misc</b></summary>

- `Library in The Backrooms.pdf`  Algorithmic Search. Pencarian string spesifik di Library of Babel berdasarkan koordinat heksadesimal.
- `Tes Kejiwaan.pdf`  Visual Puzzle. Memutar balik gambar (rotasi 180 derajat) untuk membaca flag.
- `Soal UTBK.pdf`  Substitution Logic. Memecahkan pola substitusi karakter sederhana berdasarkan konteks soal.

</details>
