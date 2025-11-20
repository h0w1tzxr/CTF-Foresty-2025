<div align="center">

<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTZyPzorKkQfJFLlR7fuzNEKp3lCXvE3s5-9Q&s" height="120" alt="Logo Foresty Lab" style="border-radius: 15px; box-shadow: 0px 0px 20px rgba(0,0,0,0.5);">

# 🌲 CTF Foresty 2025 Write-Ups
**Capture The Flag Documentation**
<br>
_Authored by **Constantine**_

<div style="display: flex; justify-content: center; gap: 10px; margin-top: 10px;">
  <img src="https://img.shields.io/badge/Status-Finished-success?style=for-the-badge&logo=cachet">
  <img src="https://img.shields.io/badge/Flags%20Captured-24%20%2F%2026-blueviolet?style=for-the-badge&logo=ctf">
  <img src="https://img.shields.io/badge/Focus-Red%20Teaming-red?style=for-the-badge">
</div>

---

</div>

## 💥 Binary Exploitation

> **Mission:** Memory corruption, buffer overflows, dan manipulasi register.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Baby Pwn** | 230 | 🟢 | **Buffer Overflow**. Overwrite variabel return tanpa proteksi Canary. | [📄 PDF](Binary%20Exploitation/Baby%20Pwn.pdf) |
| **Karbit Checker** | 290 | 🟢 | **Ret2Win**. `gets()` vuln, overwrite RIP ke fungsi `give_flag`. | [📄 PDF](Binary%20Exploitation/Karbit%20Checker.pdf) |
| **Pemanasan-1** | 220 | 🟢 | **Stack Alignment**. Ret2Win + tambah gadget `RET` kosong untuk fix segfault movaps. | [📄 PDF](Binary%20Exploitation/pemanasan-1.pdf) |

<br>

## 🔐 Cryptography

> **Mission:** Memecahkan sandi klasik dan eksploitasi kelemahan RSA.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Operation Foresty** | 320 | 🟡 | **Multi-layer Decryption**. Reverse pipeline: Transposition -> Hill -> Affine -> Vig -> Subst -> ROT13. | [📄 PDF](Crypto/Operation%20Foresty.pdf) |
| **RSA Shared Prime** | 100 | 🟢 | **Common Factor Attack**. Menghitung GCD dari dua modulus ($n$) untuk mencari $p$. | [📄 PDF](Crypto/RSA%20Shared%20Prime.pdf) |

<br>

## 🔎 Digital Forensics

> **Mission:** Analisis struktur file, perbaikan header, dan ekstraksi metadata.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Cropped Top** | 310 | 🟡 | **Header Repair**. Fix tinggi gambar (IHDR chunk) pada PNG yang "terpotong". | [📄 PDF](Forensic/Cropped%20Top.pdf) |
| **Meta** | 100 | 🟢 | **Office XML**. Unzip `.docx`, temukan hidden comment di XML untuk password zip. | [📄 PDF](Forensic/Meta.pdf) |
| **Secretfile** | 100 | 🟢 | **Recursive Zip**. Scripting Python untuk ekstrak zip bertingkat (Matryoshka). | [📄 PDF](Forensic/Secretfile.pdf) |
| **Sound** | 100 | 🟢 | **Audio Spectrum**. Analisis waveform audio untuk melihat Morse code. | [📄 PDF](Forensic/Sound.pdf) |
| **Tutut** | 100 | 🟢 | **Multi-stage**. Audio Morse -> Link WA -> Metadata Exif pada gambar. | [📄 PDF](Forensic/Tutut.pdf) |

<br>

## 🕵️ Open Source Intelligence

> **Mission:** Geolocating, tracking jejak digital, dan threat intelligence.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Atmin Lagi** | 100 | 🟢 | **GeoINT**. Identifikasi Bandara Jambi via plat nomor kendaraan & arsitektur. | [📄 PDF](OSINT/Atmin%20Lagi.pdf) |
| **Atmint** | 100 | 🟢 | **IMINT**. Presisi lokasi Shelter Kalayang Soetta (CGK) via signage & arsitektu. | [📄 PDF](OSINT/Atmint.pdf) |
| **Serlok** | 100 | 🟢 | **Visual Recon**. Zoom in teks samar "Stigm" -> Stigma Billiard. | [📄 PDF](OSINT/Serlok.pdf) |
| **Thr34t_4ct0r** | 430 | 🔴 | **Dark Web Profiling**. Lookup database BreachForums untuk de-anonimisasi aktor. | [📄 PDF](OSINT/Thr34t_4ct0r.pdf) |

<br>

## ⚙️ Reverse Engineering

> **Mission:** Decompile bytecode dan analisis alur logika program.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Baby Reveng** | 100 | 🟢 | **Array Deobfuscation**. Reversing logika XOR & aritmatika pada array integer. | [📄 PDF](Reveng/Baby%20Reveng.pdf) |
| **Byte Circus** | 100 | 🟢 | **Python Bytecode**. Decompile `.pyc` (Python 3.13) dan reverse math logic. | [📄 PDF](Reveng/Byte-Circus.pdf) |
| **Ini Chall Reverse?** | 100 | 🟢 | **Static Analysis**. Flag ditemukan plain-text menggunakan command `strings`. | [📄 PDF](Reveng/Ini%20Challenge%20Reverse?.pdf) |

<br>

## 🌐 Web Exploitation

> **Mission:** Injection, Broken Access Control, dan RCE.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **iHGracias** | 100 | 🟢 | **IDOR & Cookie**. Manipulasi cookie role & IDOR pada parameter user ID. | [📄 PDF](Web%20Exploit/iHGracias.pdf) |
| **Injection** | 110 | 🟢 | **SQLi & Cmd Inj**. Bypass login via SQLi, lalu RCE via fitur "Ping". | [📄 PDF](Web%20Exploit/Injection.pdf) |
| **Restricted Area** | 100 | 🟢 | **Client-side**. Flag tersembunyi di atribut `value` input HTML. | [📄 PDF](Web%20Exploit/Restricted%20Area.pdf) |
| **Toko Bendera** | 450 | 🔴 | **DomPDF RCE**. Exploitasi font caching untuk eksekusi RCE pada DompPDF. | [📄 PDF](Web%20Exploit/Toko%20Bendera.pdf) |

<br>

## 🎲 Miscellaneous

> **Mission:** Logic puzzle, algoritma, dan problem solving unik.

| Challenge | Pts | Diff | ⚡ Critical Insight (TL;DR) | Report |
| :--- | :---: | :---: | :--- | :---: |
| **Library Backrooms**| 330 | 🟡 | **Algo Search**. Pencarian koordinat hex spesifik di Library of Babel. | [📄 PDF](Misc/Library%20in%20The%20Backrooms.pdf) |
| **Soal UTBK** | 100 | 🟢 | **Logic Cipher**. Substitusi karakter sederhana (1=F, 2=O, dst). | [📄 PDF](Misc/Soal%20UTBK.pdf) |
| **Tes Kejiwaan** | 100 | 🟢 | **Visual Logic**. Memutar gambar 180 derajat untuk membaca teks. | [📄 PDF](Misc/Tes%20Kejiwaan.pdf) |

---

<div align="center">

### 🛠️ Arsenal & Tools
<br>
<img src="https://img.shields.io/badge/Pwntools-557C94?style=flat-square&logo=kali-linux&logoColor=white">
<img src="https://img.shields.io/badge/Ghidra-557C94?style=flat-square&logo=kali-linux&logoColor=white">
<img src="https://img.shields.io/badge/CyberChef-3C3C3C?style=flat-square&logo=chef&logoColor=white">
<img src="https://img.shields.io/badge/Google%20Dorking-4285F4?style=flat-square&logo=google&logoColor=white">
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white">
<img src="https://img.shields.io/badge/ChatGPT%205.1%20Thinking-74aa9c?logo=openai&logoColor=white">
<img src="https://img.shields.io/badge/Google%20Gemini%202.5%20Pro-886FBF?logo=googlegemini&logoColor=fff">

<br><br>
<i>"The Lion Doesn't Concern Himself Designing A Write-Up At 3 AM."</i>
</div>
