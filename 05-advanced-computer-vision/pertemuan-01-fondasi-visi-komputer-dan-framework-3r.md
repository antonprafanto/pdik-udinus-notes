# 📌 Catatan Perkuliahan: Visi Komputer Lanjut (Pertemuan 1)
**Mata Kuliah:** Advanced Computer Vision (Visi Komputer Lanjut)  
**Dosen Pengampu:** Dr. M. Arief Soeleman, M.Kom. (Dosen PDIK & Kaprodi MTI UDINUS)  
**Program:** Program Doktor Ilmu Komputer (PDIK) - Universitas Dian Nuswantoro (UDINUS)  
**Waktu:** Perkuliahan Perdana Semester Gasal 2026/2027  

---

## 🧭 Pendahuluan & Orientasi Perkuliahan

Perkuliahan perdana mata kuliah **Visi Komputer Lanjut (Advanced Computer Vision)** diampu oleh **Dr. M. Arief Soeleman, M.Kom.**. Dr. Arief memaparkan bahwa visi komputer merupakan salah satu cabang ilmu komputasi dengan laju perkembangan tercepat, didorong oleh perpaduan antara kecerdasan buatan (*AI/Deep Learning*) dan inovasi perangkat sensor visual.

* **Target Akhir Perkuliahan:** Mahasiswa diwajibkan menyelesaikan **Project Riset Computer Vision** yang menitikberatkan pada kontribusi pengembangan metode. Pada semester berikutnya, hasil proyek ini dapat ditingkatkan menjadi naskah publikasi ilmiah.
* **Buku Rujukan Utama:** *Richard Szeliski - Computer Vision: Algorithms and Applications*.

---

## 1. 🧱 Kerangka Kerja Klasik 3R dalam Computer Vision

Dr. Arief membedah permasalahan klasik dalam komputasi visual ke dalam formula **3R**:

```
                 ┌───────────────────────────────────────────────────────────┐
                 │    THE CLASSIC 3R FRAMEWORK IN COMPUTATIONAL VISION       │
                 └─────────────────────────────┬─────────────────────────────┘
                                               │
         ┌─────────────────────────────────────┼─────────────────────────────────────┐
         ▼                                     ▼                                     ▼
┌──────────────────┐                 ┌──────────────────┐                  ┌──────────────────┐
│  RECONSTRUCTION  │                 │   RECOGNITION    │                  │  REORGANIZATION  │
│  (3D World Form) │                 │  (What is inside)│                  │(Context & Scene) │
├──────────────────┤                 ├──────────────────┤                  ├──────────────────┤
│• 2D to 3D Shape  │                 │• Detection (Box) │                  │• Semantic Segm.  │
│• Depth Estimat.  │───────────────► │• Classification  │────────────────► │• Relational Scene│
│• Candi/Heritage  │                 │• Fine-grained    │                  │• Image Captioning│
│  Restoration     │                 │  Identification  │                  │• Scene Synthesis │
└──────────────────┘                 └──────────────────┘                  └──────────────────┘
```

### A. Reconstruction (What does the world look like?)
* **Definisi:** Membangun kembali informasi geometri, bentuk 3 dimensi, dan struktur ruang nyata dari data visual 2D.
* **Domain Aplikasi:**
  - Pemodelan ulang 3D bangunan gedung dan kendaraan.
  - Rekonstruksi cagar budaya (*digital cultural heritage*), seperti merekonstruksi bagian patung atau relief candi purbakala yang patah/rusak secara digital.
  - *Depth estimation* dan pemetaan spasial pada kendaraan otonom.

### B. Recognition (What is in the image?)
* **Definisi:** Tugas komputasi untuk mengenali entitas apa saja yang terdapat di dalam data citra atau video.
* **Hierarki Tugas Visual:**
  1. **Detection (Tugas Fundamental):** Merasakan keberadaan objek dan mengunci koordinat posisinya (*bounding box*). Deteksi adalah gerbang awal mutlak; analisis lanjutan tidak akan pernah berhasil jika objeknya saja gagal dideteksi.
  2. **Classification:** Mengelompokkan citra secara global ke dalam label kelas tertentu.
  3. **Fine-Grained Recognition:** Mengidentifikasi detail spesifik (misal: bukan sekadar daun, melainkan jenis hama/patogen yang menyerang).

### C. Reorganization (How are things arranged and related?)
* **Definisi:** Memahami konteks, susunan spasial, dan relasi semantik antar objek dalam *scene*:
  - **Semantic Segmentation:** Pelabelan per piksel (misal: area pohon hijau, manusia merah, marka jalan kuning).
  - **Image Captioning & Scene Understanding:** Menghasilkan narasi kontekstual dari citra (misal: menceritakan aktivitas pejalan kaki di zebra cross).

---

## 2. 🌧️ Menemukan Novelty dari Tantangan Lingkungan Riil

Dr. Arief menegaskan bahwa riset doktoral tidak boleh hanya menguji algoritma pada dataset laboratorium yang bersih. Kebaruan (*novelty*) seringkali lahir dari keberhasilan menyelesaikan gangguan visual ekstrem di dunia nyata:
* **Perubahan Iluminasi (*Illumination Changes*):** Transisi cahaya ekstrem dari siang ke senja/malam, bayangan tajam (*hard shadows*), atau ruangan minim cahaya.
* **Oklusi (*Occlusion*):** Objek target terhalang sebagian oleh objek lain (misal: pekerja atau pengendara yang posisinya saling menutupi).
* **Gangguan Cuaca & Partikel Udara:** Kabut tebal, asap kebakaran hutan (fenomena riil di Kalimantan), atau hujan lebat yang menuntut teknik *dehazing / defogging*.

---

## 3. 🗺️ Desain Roadmap Riset 5 Tahun (Disertasi & Hibah BIMA)

Dr. Arief membagikan formula praktis menyusun peta jalan riset (*research roadmap*) bertahap agar topik disertasi mahasiswa dapat didanai oleh skema Hibah Kemdiktisaintek (BIMA):
* **Tahun 1:** *Image Classification* (Klasifikasi citra kondisi A vs B).
* **Tahun 2:** *Object Detection* (Menemukan lokasi bounding box pada citra multi-skala).
* **Tahun 3:** *Fine-Grained Recognition & Severity Grading* (Mengidentifikasi jenis dan tingkat keparahan anomali).
* **Tahun 4:** *Prototyping on Mobile/Edge Devices* (Implementasi mandiri pada smartphone/kamera otonom tanpa tergantung PC server).
* **Tahun 5:** *Hilirisasi & Pengujian Lapangan Industri / UMKM*.

---
*Catatan ini dirangkum dari perkuliahan perdana Visi Komputer Lanjut PDIK UDINUS untuk keperluan belajar mandiri dan berbagi pengetahuan.*
