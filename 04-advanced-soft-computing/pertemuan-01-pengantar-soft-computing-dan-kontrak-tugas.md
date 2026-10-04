# 📌 Catatan Perkuliahan: Komputasi Lunak Lanjut (Pertemuan 1)
**Mata Kuliah:** Advanced Soft Computing (Komputasi Lunak Lanjut)  
**Dosen Pengampu:** Prof. Dr. A. Zainul Fanani, S.Si., M.Kom. (Tim Dosen: Prof. Dr. Nova, Dr. Ruri)  
**Program:** Program Doktor Ilmu Komputer (PDIK) - Universitas Dian Nuswantoro (UDINUS)  
**Waktu:** Perkuliahan Perdana Semester Gasal 2026/2027  

---

## 🧭 Pendahuluan & Filosofi Asesmen Doktoral

Perkuliahan perdana mata kuliah **Komputasi Lunak Lanjut (Advanced Soft Computing)** diampu oleh **Prof. Dr. A. Zainul Fanani, S.Si., M.Kom.**. Prof. Fanani menegaskan bahwa iklim asesmen pada jenjang Doktor (S3) berorientasi 100% pada **Project/Output-Based Learning**:

* **Bebas Ujian Tertulis Konvensional (UTS / UAS):** Evaluasi perkuliahan berpusat pada penugasan riset bertahap yang diselaraskan langsung dengan **rencana topik Disertasi S3**.
* **Target Output:** Di akhir semester, mahasiswa diharapkan telah menghasilkan **draf naskah ilmiah siap *submit* ke International Conference terindeks Scopus (IEEE/ACM/Scopus)**.

---

## 1. 📅 Roadmap 3 Tugas Berkelanjutan (Semester 1)

Penugasan perkuliahan dirancang terstruktur dalam 3 tahapan yang saling menyambung:

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
```

### 🔹 Tugas 1: Usulan Topik & Review 7 Paper Scopus (Deadline: ~Minggu ke-4)
1. **Penyusunan Usulan:** Menuliskan topik/judul penelitian yang sedang tren dan relevan dengan kepakaran.
2. **Komponen:**
   - Judul & Topik Penelitian
   - Pendahuluan / Latar Belakang Masalah
   - Rumusan Masalah (Research Questions: RQ1, RQ2, RQ3)
   - Tujuan Penelitian (Research Objectives: RO1, RO2, RO3)
3. **Review Literatur:** Mengulas **minimal 7 paper Scopus (5 tahun terakhir)** yang paling relevan dengan topik usulan ($\sim$ setengah halaman per paper: metode, capaian hasil, keunggulan, dan kelemahan/gap).
4. **Presentasi:** Dipresentasikan ringkas ($\sim$ 10 menit) untuk mendapatkan masukan dosen dan rekan kelas.

### 🔹 Tugas 2: Proposed Method & Metodologi / Bab 3 (Deadline: ~Minggu ke-8/9)
1. Menguraikan metode yang diusulkan (*proposed method*) atau algoritma baru/modifikasi.
2. Menyusun diagram alir tahapan eksperimen:
   $$\text{Dataset} \longrightarrow \text{Preprocessing} \longrightarrow \text{Eksperimen Pemodelan} \longrightarrow \text{Evaluasi / Validasi}$$
3. Mengidentifikasi di mana letak instrumen Soft Computing (optimasi, hybrid, ensemble) akan disematkan untuk meningkatkan performa sistem.

### 🔹 Tugas 3: Eksperimen Baseline & Draf Paper Publikasi IMRaD (Deadline: ~Minggu ke-14)
1. Melakukan eksperimen awal (*baseline experiment*) menggunakan data publik/privat.
2. Menyusun draf naskah paper berstandar internasional dengan format **IMRaD** (*Introduction, Methods, Results, and Discussion*).
3. Luaran: Paper siap submit ke *International Conference* terindeks Scopus.

---

## 2. 🧠 Peran Soft Computing dalam Melahirkan Novelty S3

Prof. Fanani menekankan bahwa riset doktoral wajib menghadirkan **Improvement / Perbaikan Metode**, bukan sekadar menerapkan metode lama ke objek/data baru (level sarjana).

* **Tahun 1 (Membangun Baseline):** Ujikan metode *state-of-the-art* (misal: CNN, LSTM, Transformer) pada domain masalah yang belum pernah dicoba. Jika hasil akurasi baseline masih memiliki kelemahan, diskusikan secara objektif dalam sesi *Discussion* paper konferensi.
* **Tahun 2 & 3 (Injeksi Soft Computing untuk Disertasi & Jurnal):** Perbaiki kelemahan baseline menggunakan teknik Soft Computing:
  1. **Swarm Intelligence & Optimasi (PSO, ACO, Bee Colony):** Untuk optimasi hyperparameter, seleksi fitur, dan penyesuaian bobot adaptif.
  2. **Evolutionary Algorithms (Genetic Algorithm):** Untuk pencarian arsitektur optimal (*Neural Architecture Search*) dan optimasi multi-objektif.
  3. **Ensemble Learning:** Menggabungkan multi-model untuk meningkatkan generalisasi dan ketahanan prediksi.
  4. **Hybrid Methods (Neuro-Fuzzy / ANFIS):** Menggabungkan logika fuzzy dengan jaringan saraf tiruan.

---

## 3. 💡 Tips Praktis Pengumpulan Referensi

* Untuk tugas kuliah ini, pilih **7 paper Scopus yang paling mendekati (*mirror topic*)**.
* Namun, seluruh paper lain yang sudah dikumpulkan (misal 50–100 paper) **jangan dibuang**. Simpan semuanya sebagai modal berharga untuk menyusun naskah disertasi dan proposal komprehensif.

---

## 4. 🤝 Kolaborasi & Kekompakan Angkatan 2026

* Prof. Fanani menyarankan agar mahasiswa angkatan 2026 membuat grup mandiri untuk saling mendukung, berdiskusi mengenai kebuntuan algoritma/koding, dan bertukar wawasan metodologi.
* Manfaatkan semester 1 ini untuk menyiapkan modal riset dan literatur yang matang, sehingga saat pembagian Promotor di Semester 2, calon pembimbing akan langsung menyetujui usulan riset kita.

---
*Catatan ini dirangkum dari perkuliahan perdana Komputasi Lunak Lanjut PDIK UDINUS untuk keperluan belajar mandiri dan berbagi pengetahuan.*
