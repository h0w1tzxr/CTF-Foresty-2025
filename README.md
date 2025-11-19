<div align="center">

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZyPzorKkQfJFLlR7fuzNEKp3lCXvE3s5-9Q&s" height="150" alt="Logo Foresty Lab">

# 🌲 CTF Foresty 2025 Write-Ups
**Documentation & Solver Scripts by Constantine**

<p>
  <img src="https://img.shields.io/badge/Category-Jeopardy-0f172a?style=for-the-badge&logo=distrobox" alt="Category">
  <img src="https://img.shields.io/badge/Solved-24%20Challenges-10b981?style=for-the-badge&logo=cachet" alt="Solved Status">
</p>

---
<br>
Repository ini berisi write-up dari kompetisi CTF Foresty 2025.

</div>

## 🗺️ NavHub

Berikut adalah rekap challenge yang telah diselesaikan. Klik pada **Nama Kategori** untuk melihat detail write-up dan teknik yang digunakan.

| Kategori | Jumlah Solved | Key Topics |
| :--- | :---: | :--- |
| **Binary Exploitation** | 3 | Buffer Overflow, Ret2Win, Stack Alignment |
| **Cryptography** | 2 | RSA Common Factor, Classical Cipher Stack |
| **Forensics** | 5 | Audio Analysis, Metadata, Header Repair, Recursive Zip |
| **OSINT** | 4 | GeoINT, Threat Actor Profiling |
| **Reverse Engineering** | 3 | Decompilation (.pyc), Stack Strings, Static Analysis |
| **Web Exploitation** | 4 | SQLi, RCE, DomPDF, IDOR, Cookie Tampering |
| **Misc** | 3 | Logic Puzzle, Algorithmic Search |

---

## 📂 Write-Ups

<details>
<summary><h3>💥 Binary Exploitation (Pwn)</h3></summary>

> **Focus:** Stack-based buffer overflows and return-oriented programming basics.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Baby Pwn** | Baby | **Variable Overwrite**. Overflow buffer untuk menimpa variabel return tanpa proteksi Canary. | [Read PDF](Binary%20Exploitation/Baby%20Pwn.pdf) |
| **Karbit Checker** | Easy | **Ret2Win**. Memanfaatkan fungsi `gets()` untuk menimpa RIP ke fungsi `give_flag`. | [Read PDF](Binary%20Exploitation/Karbit%20Checker.pdf) |
| **Pemanasan-1** | Easy-Med | **Stack Alignment**. Teknik Ret2Win dengan menambahkan gadget `RET` kosong untuk fix movaps segfault. | [Read PDF](Binary%20Exploitation/pemanasan-1.pdf) |

</details>

<details>
<summary><h3>🔐 Cryptography</h3></summary>

> **Focus:** Classical ciphers and RSA misconfigurations.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Operation Foresty** | Med-Hard | **Multi-layer Decoding**. Columnar Transposition -> Hill -> Affine -> Vigenère -> Substitution -> ROT13. | [Read PDF](Crypto/Operation%20Foresty.pdf) |
| **RSA Shared Prime** | Easy | **Common Factor Attack**. Menyerang dua public key yang berbagi satu faktor prima ($p$) yang sama. | [Read PDF](Crypto/RSA%20Shared%20Prime.pdf) |

</details>

<details>
<summary><h3>🔎 Digital Forensics</h3></summary>

> **Focus:** File structure analysis, steganography, and automation.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Cropped Top** | Easy | **Header Repair**. Memperbaiki chunk `IHDR` pada PNG untuk mengembalikan dimensi gambar asli. | [Read PDF](Forensic/Cropped%20Top.pdf) |
| **Meta** | Easy-Med | **Office XML**. Menemukan hidden comment di dalam struktur XML `.docx` untuk password zip. | [Read PDF](Forensic/Meta.pdf) |
| **Secretfile** | Easy | **Scripting**. Otomatisasi ekstraksi file ZIP bertingkat (Matryoshka) menggunakan Python. | [Read PDF](Forensic/Secretfile.pdf) |
| **Sound** | Easy | **Audio Analysis**. Menganalisis spektrum waveform untuk decoding Morse code. | [Read PDF](Forensic/Sound.pdf) |
| **Tutut** | Easy | **Multi-stage**. Kombinasi analisis Audio (Morse) -> URL -> Ekstraksi Metadata Gambar. | [Read PDF](Forensic/Tutut.pdf) |

</details>

<details>
<summary><h3>🕵️ OSINT (Open Source Intelligence)</h3></summary>

> **Focus:** Geolocation (IMINT) and digital footprint analysis.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Atmin Lagi** | Easy | **GeoINT**. Identifikasi lokasi parkiran bandara (Jambi) berdasarkan plat nomor dan arsitektur. | [Read PDF](OSINT/Atmin%20Lagi.pdf) |
| **Atmint** | Easy-Med | **IMINT**. Presisi lokasi shelter Kalayang Bandara Soetta berdasarkan refleksi dan signage. | [Read PDF](OSINT/Atmint.pdf) |
| **Serlok** | Easy | **Visual Recon**. Identifikasi lokasi Billiard hanya dari teks samar "Stigm" di latar belakang. | [Read PDF](OSINT/Serlok.pdf) |
| **Thr34t_4ct0r** | Med-Hard | **Profiling**. Melacak identitas asli aktor data leak menggunakan BreachForums DB lookup. | [Read PDF](OSINT/Thr34t_4ct0r.pdf) |

</details>

<details>
<summary><h3>⚙️ Reverse Engineering</h3></summary>

> **Focus:** Static analysis and bytecode decompilation.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Baby Reveng** | Easy | **Deobfuscation**. Analisis stack strings di Ghidra dan membalikkan logika penjumlahan array. | [Read PDF](Reveng/Baby%20Reveng.pdf) |
| **Byte Circus** | Easy | **PyDecomp**. Decompile `.pyc` ke `.py` dan membalikkan logika XOR sederhana. | [Read PDF](Reveng/Byte-Circus.pdf) |
| **Ini Chall Reverse?** | Baby | **Strings**. Pengambilan flag secara langsung menggunakan command `strings` pada binary. | [Read PDF](Reveng/Ini%20Challenge%20Reverse?.pdf) |

</details>

<details>
<summary><h3>🌐 Web Exploitation</h3></summary>

> **Focus:** Injection attacks, IDOR, and CVE exploitation.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **iHGracias** | Easy-Med | **IDOR & PrivEsc**. Manipulasi cookie untuk jadi admin dan akses data user lain. | [Read PDF](Web%20Exploit/iHGracias.pdf) |
| **Injection** | Easy-Med | **SQLi & Command Injection**. Auth bypass via SQLi dan RCE via fitur ping. | [Read PDF](Web%20Exploit/Injection.pdf) |
| **Restricted Area** | Baby | **Source Code**. Menemukan flag di atribut `value` HTML input yang tersembunyi. | [Read PDF](Web%20Exploit/Restricted%20Area.pdf) |
| **Toko Bendera** | Med-Hard | **DomPDF RCE**. Exploitasi kerentanan font caching DomPDF untuk eksekusi PHP jarak jauh. | [Read PDF](Web%20Exploit/Toko%20Bendera.pdf) |

</details>

<details>
<summary><h3>🎲 Miscellaneous</h3></summary>

> **Focus:** Logic puzzles and algorithmic thinking.

| Challenge | Difficulty | Technique Used | File |
| :--- | :---: | :--- | :--- |
| **Library Backrooms**| Med | **Algo Search**. Pencarian string spesifik di Library of Babel via koordinat hex. | [Read PDF](Misc/Library%20in%20The%20Backrooms.pdf) |
| **Soal UTBK** | Easy | **Logic**. Substitusi karakter sederhana berdasarkan pola soal. | [Read PDF](Misc/Soal%20UTBK.pdf) |
| **Tes Kejiwaan** | Easy | **Visual**. Memutar balik gambar (rotasi 180 derajat) untuk membaca flag. | [Read PDF](Misc/Tes%20Kejiwaan.pdf) |

</details>

---

<div align="center">
  
**Tools & Assistance:**
<br>
![Pwntools](https://img.shields.io/badge/Pwntools-557C94?style=flat&logo=kali-linux&logoColor=white)
![Ghidra](https://img.shields.io/badge/Ghidra-557C94?style=flat&logo=kali-linux&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![ChatGPT](https://img.shields.io/badge/ChatGPT%205.1%20Thinking-74aa9c?logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Google%20Gemini%202.5%20Pro-886FBF?logo=googlegemini&logoColor=fff)

<br>
</div>
