# 📌 Catatan Perkuliahan: Komputasi Lunak Lanjut (Pertemuan 1)
**Mata Kuliah:** Advanced Soft Computing (Komputasi Lunak Lanjut)  
**Dosen Pengampu:** Prof. Dr. A. Zainul Fanani, S.Si., M.Kom. (Tim Dosen: Prof. Dr. Nova, Dr. Ruri)  
**Program:** Program Doktor Ilmu Komputer (PDIK) - Universitas Dian Nuswantoro (UDINUS)  
**Waktu:** Perkuliahan Perdana Semester Gasal 2026/2027 (~68 menit)  

---

## 🧭 Pendahuluan & Filosofi Asesmen Doktoral

Perkuliahan perdana mata kuliah **Komputasi Lunak Lanjut (Advanced Soft Computing)** diampu oleh **Prof. Dr. A. Zainul Fanani, S.Si., M.Kom.**. Prof. Fanani menegaskan bahwa iklim asesmen pada jenjang Doktor (S3) berorientasi 100% pada **Project & Output-Based Learning**:

* **Bebas Ujian Tertulis Konvensional (UTS / UAS):** Evaluasi perkuliahan berpusat pada penugasan riset bertahap yang diselaraskan langsung dengan **rencana topik Disertasi S3**.
* **Jaminan Penilaian Objektif:** Mahasiswa yang pada akhir semester telah menyelesaikan naskah paper siap submit dijamin memperoleh nilai yang sangat memuaskan (*"nilainya otomatis apik lah ngono wae"*).
* **Kewajiban Publikasi Doktoral UDINUS (Arahan Prof. Aris):**  
  Mahasiswa S3 diwajibkan menghasilkan minimal 2 publikasi Scopus:
  1. *Publikasi 1 (Pra-Proposal):* International Conference Scopus (IEEE/ACM) sebagai syarat maju Ujian Proposal Disertasi. **(Ditargetkan langsung dari Tugas 3 mata kuliah ini!)**
  2. *Publikasi 2 (Kelulusan Disertasi):* Jurnal Internasional Bereputasi Scopus (Q1/Q2) yang memuat perbaikan metode (*method improvement*).
* **Target Output:** Di akhir semester, mahasiswa menghasilkan **draf naskah ilmiah format IMRaD siap *submit* ke International Conference terindeks Scopus (IEEE/ACM/Scopus)**.

```
                    ┌─────────────────────────────────────────────────────────────┐
                    │     ROADMAP TUGAS BERKELANJUTAN KOMPUTASI LUNAK             │
                    └──────────────────────────────┬──────────────────────────────┘
                                                   │
             ┌─────────────────────────────────────┼─────────────────────────────────────┐
             ▼                                     ▼                                     ▼
    ┌──────────────────┐                 ┌──────────────────┐                  ┌──────────────────┐
    │   TUGAS 1        │                 │   TUGAS 2        │                  │   TUGAS 3        │
    │ (Minggu ke-4)    │                 │ (Minggu ke-8/9)  │                  │ (Minggu ke-14)   │
    ├──────────────────┤                 ├──────────────────┤                  ├──────────────────┤
    │• Topik Disertasi │                 │• Proposed Method │                  │• Baseline Exper. │
    │• Pendahuluan/RQ  │───────────────► │• Diagram Alir    │────────────────► │• Draf Paper IMRaD│
    │• Review Min. 7   │                 │  Bab 3 Riset     │                  │• Siap Submit     │
    │  Paper Scopus    │                 │• Peran Soft Comp.│                  │  (Scopus Conf.)  │
    └──────────────────┘                 └──────────────────┘                  └──────────────────┘
             │                                                                     ▲
             └────────────── BERKONTRIBUSI LANGSUNG KE DISERTASI S3 ───────────────┘
```

---

## 1. 📅 Roadmap 3 Tugas Berkelanjutan (Semester 1)

Penugasan perkuliahan dirancang terstruktur dalam 3 tahapan yang saling menyambung:

### 🔹 Tugas 1: Usulan Topik & Review 7 Paper Scopus (Deadline: ~Minggu ke-4)
1. **Penyusunan Usulan:** Menuliskan topik/judul penelitian yang sedang tren dan relevan dengan kepakaran.
2. **Komponen Pendahuluan:**
   * Judul & Topik Penelitian
   * Pendahuluan / Latar Belakang Masalah empiris
   * Rumusan Masalah: *Research Questions* (RQ1, RQ2, RQ3)
   * Tujuan Penelitian: *Research Objectives* (RO1, RO2, RO3)
3. **Review Literatur:** Mengulas **minimal 7 paper Scopus (5 tahun terakhir)** yang paling relevan dengan topik usulan ($\sim 0,5$ halaman per paper, total $\sim 3,5$ halaman: masalah, metode, capaian hasil, keunggulan, serta kelemahan/gap).
4. **Penetapan "Paper Acuan" (Baseline Benchmark Paper):**  
   Dari 7 paper yang direview, mahasiswa **wajib menunjuk 1 paper utama sebagai Paper Acuan (Riset Acuan)**. Paper acuan inilah yang menjadi lawan tanding (*benchmark*) di mana kelemahannya akan diperbaiki dan metrik performanya akan dikalahkan oleh metode usulan kita.
5. **Presentasi:** Dipresentasikan ringkas ($\sim 10$ menit per mahasiswa) untuk mendapatkan masukan dosen dan rekan sekelas.

### 🔹 Tugas 2: Proposed Method & Metodologi / Bab 3 (Deadline: ~Minggu ke-8/9)
1. Menguraikan metode yang diusulkan (*proposed method*) atau kombinasi algoritma baru.
2. Menyusun diagram alir tahapan eksperimen standar Bab 3:
   $$\text{Dataset (Publik/Privat)} \longrightarrow \text{Preprocessing} \longrightarrow \text{Eksperimen Pemodelan} \longrightarrow \text{Evaluasi / Validasi}$$
3. Mengidentifikasi secara eksplisit di mana letak instrumen Soft Computing (optimasi, hybrid, ensemble) akan disematkan untuk meningkatkan performa sistem.

### 🔹 Tugas 3: Eksperimen Baseline & Draf Paper Publikasi IMRaD (Deadline: ~Minggu ke-14)
1. Melakukan eksperimen awal (*baseline experiment*) menggunakan data benchmark publik atau studi kasus mandiri.
2. Menyusun draf naskah paper berstandar internasional dengan format **IMRaD** (*Introduction, Methods, Results, and Discussion*).
3. Luaran: Paper siap submit ke *International Conference* terindeks Scopus (IEEE/ACM/Scopus).

---

## 2. 🧠 Peran Soft Computing dalam Melahirkan Novelty S3

Prof. Fanani menekankan bahwa riset doktoral wajib menghadirkan **Improvement / Perbaikan Metode**, bukan sekadar menerapkan metode lama ke objek/data baru (level sarjana).

* **Tahun 1 (Membangun Baseline):**  
  Ujikan metode *state-of-the-art* (Deep Learning, CNN, LSTM, Transformer) pada domain masalah yang belum pernah dicoba orang lain. Jika hasil akurasi baseline masih lebih rendah dari metode pembanding (misal: akurasi kita 94% sedangkan pembanding 96%), **itu wajar dan sah**. Kelemahan tersebut diulas secara jujur dalam sesi *Discussion* paper konferensi.
* **Tahun 2 & 3 (Injeksi Soft Computing untuk Disertasi & Jurnal Q1/Q2):**  
  Kelemahan baseline tahun pertama diperbaiki menggunakan 4 pilar instrumen Soft Computing:
  1. **Swarm Intelligence & Optimasi (PSO, ACO, Bee Colony):** Untuk optimasi hyperparameter, seleksi fitur, dan penyesuaian bobot adaptif.
  2. **Evolutionary Algorithms (Genetic Algorithm):** Untuk pencarian arsitektur optimal (*Neural Architecture Search*) dan optimasi multi-objektif.
  3. **Ensemble Learning:** Menggabungkan multi-model (Stacking, Boosting) untuk meningkatkan generalisasi dan mereduksi bias/variansi.
  4. **Hybrid Methods (Neuro-Fuzzy / ANFIS):** Menggabungkan logika fuzzy dengan jaringan saraf tiruan untuk penalaran ketidakpastian.

---

## 3. 💡 Tips Praktis Pengumpulan Referensi & Kesiapan Promotor

* **Jangan Buang Paper yang Terkumpul:** Untuk tugas ini pilih 7 paper Scopus yang paling mendekati (*mirror topic*). Namun, seluruh paper lain yang sudah diunduh (misal 50–100 paper) simpan semuanya sebagai modal berharga naskah disertasi.
* **Modal Kuat Menghadapi Promotor di Semester 2:**  
  Saat pembagian promotor dilakukan di Semester 2, mahasiswa yang sudah memiliki katalog literatur rapi, rumusan RQ/RO, bagan alir Bab 3, dan eksperimen awal baseline tidak akan dapat ditolak oleh promotor, sehingga proses bimbingan berjalan cepat dan terarah.

---

## 4. 🏛️ Pesan Sowan ke UDINUS Semarang & Solidaritas Angkatan 2026

* **Wajib Berkunjung ke Kampus UDINUS Semarang:**  
  Meskipun perkuliahan berjalan daring/hybrid, Prof. Fanani berpesan agar minimal setahun sekali mahasiswa menyempatkan diri datang ke kampus UDINUS di Semarang (minimal seminggu) untuk sowan dan berdiskusi langsung dengan calon promotor: **Prof. Dr. Aris Marjuni** (Kaprodi), **Dr. Pulung Nurtantio Andono** (Wakil Dekan / CV), **Dr. Farikhin** (Soft Computing), dan **Dr. M. Arief Soeleman** (Image Processing).  
  *Patokan Kampus:* Tepat di jantung kota Semarang dekat **Tugu Muda dan Lawang Sewu**. *"Kalau gak pernah ke Udinus jangan harap lulus dulu! 3 tahun mosok gak pernah ke Udinus."*
* **Solidaritas Angkatan 2026 (70% Mahasiswa Kalimantan):**  
  Prof. Fanani mendorong mahasiswa membuat grup mandiri angkatan 2026 untuk saling mereview draf tugas, memecahkan kebuntuan koding/algoritma, dan menjaga semangat agar seluruh rekan satu angkatan dapat lulus bersama tepat 3 tahun.
* **Format Perkuliahan Mingguan (Mulai Pertemuan 2):** $\sim 1$ jam materi teori dasar/lanjutan Soft Computing, dilanjutkan sesi interaktif bedah topik dan konsultasi progres riset mahasiswa secara bergantian satu per satu.
* **Portal Akademik & Upload Tugas:**  
  - **KULINO (`kulino.dinus.ac.id`):** LMS resmi untuk mengunduh materi dan mengunggah (*upload*) berkas Tugas 1, 2, dan 3.  
  - **SIADIN / Mahasiswa (`mhs.dinus.ac.id`):** Portal presensi perkuliahan mahasiswa per sesi.

---
*Catatan ini dirangkum dari perkuliahan perdana Komputasi Lunak Lanjut PDIK UDINUS untuk keperluan belajar mandiri dan berbagi pengetahuan.*
