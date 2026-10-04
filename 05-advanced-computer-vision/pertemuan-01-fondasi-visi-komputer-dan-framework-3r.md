# 📌 Catatan Perkuliahan: Visi Komputer Lanjut (Pertemuan 1)
**Mata Kuliah:** Advanced Computer Vision (Visi Komputer Lanjut)  
**Dosen Pengampu:** Dr. M. Arief Soeleman, M.Kom. (Dosen PDIK & Kaprodi Magister Teknik Informatika / MTI)  
**Program:** Program Doktor Ilmu Komputer (PDIK) - Universitas Dian Nuswantoro (UDINUS)  
**Semester:** Gasal 2026/2027  

---

## 🧭 Pendahuluan & Orientasi Perkuliahan

Mata kuliah **Visi Komputer Lanjut (*Advanced Computer Vision*)** pada Program Doktor Ilmu Komputer (PDIK) UDINUS diampu oleh **Dr. M. Arief Soeleman, M.Kom.** (Kaprodi MTI UDINUS). Perkuliahan ini membedah prinsip fundamental komputasi visual, evolusi dari *classical machine learning* menuju *deep learning* dan *multimodal vision*, serta strategi perumusan kebaruan (*novelty*) berbasis tantangan lingkungan dunia nyata.

### A. Literatur Rujukan Utama
1. **Richard Szeliski** – *Computer Vision: Algorithms and Applications*: Buku pegangan komprehensif yang mengkaji pemodelan geometri, ekstraksi fitur, estimasi gerak, dan aplikasi visi komputer modern.
2. **Textbook Mathematical Morphology**: Buku referensi *Mathematical Morphology for Image Processing* dari profesor tamu **TU Delft (Belanda)** yang membahas formulasi kalkulus diferensial, *thinning*, *erosion*, dan *skeletonization* citra.
3. Publikasi ilmiah mutakhir terkait arsitektur *Vision Transformer (ViT)*, *Convolutional Neural Networks (CNN)*, dan model multimodal.

### B. Skema Evaluasi & Luaran Akademik
* **Semester 1:** Mahasiswa diwajibkan menyelesaikan sebuah **Project Riset Computer Vision**. Proyek ini menitikberatkan pada **kontribusi pengembangan/perbaikan metode** (*methodological improvement*) yang aplikatif sesuai fokus riset masing-masing.
* **Semester 2:** Hasil proyek semester 1 akan ditingkatkan dan disempurnakan menjadi **naskah publikasi ilmiah (Scopus Conference / Journal)** sebagai percepatan syarat kelulusan disertasi doktoral.

---

## 1. 🧱 Kerangka Kerja Klasik 3R dalam Computer Vision

Dr. Arief Soeleman merangkum seluruh spektrum permasalahan komputasi visual ke dalam formula **The Classic 3R Framework**:

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

### A. Reconstruction (*What does the world look like?*)
* **Definisi:** Membangun kembali informasi geometri, bentuk 3 dimensi, dan struktur ruang nyata dari data visual 2D (citra tunggal atau aliran video sekuensial).
* **Implementasi:** Memproyeksikan kembali koordinat piksel 2D $(u, v)$ ke dalam ruang nyata 3D $(X, Y, Z)$ dengan memanfaatkan disparitas stereo, *Structure from Motion (SfM)*, atau *depth estimation*.
* **Studi Kasus Restorasi Cagar Budaya (*Digital Cultural Heritage*):**
  - Pemodelan ulang 3D patung dan relief candi purbakala yang mengalami kerusakan fisik (misal: bagian hidung atau telinga arca yang patah akibat cuaca dan bencana).
  - Melalui rekonstruksi visual 3D, bagian arca yang rusak dapat diprediksi dan dimodelkan kembali secara digital sesuai kaidah arsitektur aslinya.

### B. Recognition (*What is in the image?*)
* **Definisi:** Tugas komputasi untuk mengenali entitas dan objek apa saja yang termuat di dalam media visual.
* **Hierarki Tugas Komputasi Visual:**
  1. **Detection (Tugas Fundamental):**  
     Merasakan keberadaan objek dan mengunci koordinat posisinya menggunakan *bounding box*.  
     *Prinsip Dr. Arief:* Deteksi adalah pintu gerbang awal mutlak. Sistem tidak akan pernah bisa menganalisis kepatuhan helm atau pelanggaran lalu lintas jika objeknya saja gagal dideteksi.
  2. **Classification:**  
     Mengelompokkan citra secara global ke dalam label kelas diskrit (misal: memilah 50.000 citra campuran ke dalam label mobil, motor, manusia, pohon, gedung) tanpa informasi lokalisasi internal.
  3. **Fine-Grained Recognition:**  
     Menganalisis objek secara mendalam untuk membedakan variasi antar-kelas yang sangat subtil (*low inter-class variance*), seperti mengenali warna helm K3 penanda jabatan kerja (merah = safety, putih = manajemen, hijau = pekerja lingkungan) atau membedakan jenis penyakit spesifik pada daun tanaman.

### C. Reorganization (*How are things arranged and related?*)
* **Definisi:** Memahami susunan, interaksi semantik, dan relasi spasial antar-objek di dalam suatu *scene*.
* **Komputasi Tingkat Lanjut:**
  - **Semantic Segmentation:** Pelabelan semantik pada setiap piksel citra secara seragam (misal: piksel pohon diarsir hijau, piksel manusia diarsir merah, piksel jalan diarsir abu-abu).
  - **Image Captioning & Scene Understanding:** Menghasilkan narasi kontekstual yang kaya dari citra (misal: *"Seorang pria berbaju biru membawa tas ransel menyeberangi zebra cross di depan mobil putih yang sedang berhenti"*).
  - **Multimodal Vision:** Integrasi lintas modalitas data (teks-ke-citra, citra-ke-teks, audio-visual, hingga telemetri sensor IoT).

---

## 2. ⏱️ Dinamika Temporal Video & Ekstraksi Frame Rate

Pemrosesan video surveilans memiliki kompleksitas komputasi yang jauh lebih tinggi dibandingkan analisis citra statis:

1. **Formulasi Laju Frame (*Frame Rate*):**
   - Kamera video standar merekam pada laju **25 hingga 30 frame per detik (FPS)**.
   - Perekaman video selama **1 menit (60 detik)** menghasilkan:
     $$\text{Total Frame} = 60\text{ detik} \times 25\text{ FPS} = 1.500\text{ frame citra}$$
2. **Karakteristik Temporal:**
   - Dua frame yang berurutan ($\Delta t = 40\text{ ms}$) memiliki redundansi informasi yang sangat tinggi (98% piksel identik).
   - Objek dinamis (pejalan kaki atau kendaraan melaju) berpindah posisi secara cepat. Objek dapat terdeteksi pada frame 300, berpindah pada frame 400, dan hilang dari jangkauan kamera pada frame 600.
   - Diperlukan algoritma *tracking* temporal agar identitas objek (*tracking ID*) tidak tertukar saat terjadi persilangan lintasan.

---

## 3. 🌧️ Menemukan Novelty dari Tantangan Lingkungan Riil

Dr. Arief menegaskan bahwa riset doktoral tidak boleh hanya menguji algoritma pada dataset laboratorium yang bersih. **Kebaruan (*novelty*) seringkali lahir dari keberhasilan menyelesaikan gangguan visual ekstrem di dunia nyata:**

| Gangguan Lingkungan | Karakteristik Masalah | Strategi Algoritmik & Kontribusi Riset |
| :--- | :--- | :--- |
| **Perubahan Iluminasi (*Illumination Changes*)** | Transisi cahaya drastis dari siang ke malam/senja, bayangan tajam (*hard shadows*), dan *underexposure*. | *Adaptive thresholding*, normalisasi histogram, pemodelan *Fuzzy C-Means (FCM)*, dan representasi fitur invarian cahaya. |
| **Oklusi (*Occlusion*)** | Objek target terhalang sebagian oleh objek lain (misal: pengendara tanpa helm tertutup truk, daun bertumpuk). | *Part-based models*, penalaran konteks relasional spasial, dan estimasi temporal (*Kalman Filter*). |
| **Kabut & Asap (*Dehazing/Defogging*)** | Kabut pekat dan asap kebakaran hutan (fenomena riil di Kalimantan) yang mengubah pagi hari menjadi gelap gulita. | *Dark Channel Prior (DCP)*, model hamburan atmosfer fisik (*atmospheric scattering*), dan *dehazing autoencoders*. |
| **Sistem Multi-Modal** | Citra dipadukan dengan modalitas suara, teks deskriptif, dan sensor lingkungan. | *Cross-attention transformer* dan *multimodal feature fusion*. |

---

## 4. 🔬 Rekam Jejak Riset Empiris Dr. M. Arief Soeleman

Sebagai inspirasi riset, Dr. Arief membagikan pengalaman riset empiris yang telah dikembangkannya:

1. **Deteksi Objek Bergerak (*Moving Object Detection*, Cebu 2012):**
   - Menggunakan kamera statis di lantai 2 gedung kampus UDINUS Semarang.
   - Menguji pemisahan antara mobil bergerak (merah) dengan mobil parkir (putih dan hitam) di bawah terik matahari yang berubah secara dinamis.
   - Solusi: Menggabungkan **Background Subtraction** dengan **Adaptive Thresholding berbasis Fuzzy C-Means (FCM)** untuk mempertahankan ketangguhan ambang batas terhadap fluktuasi pencahayaan.
2. **Deteksi Kekerasan Video Surveilans (*Violence Detection*):**
   - Menganalisis sekuens temporal untuk mendeteksi anomali perkelahian pada ruang publik secara otomatis.
3. **Termografi UAV Drone Malam Hari (*Night Thermal UAV Vision*):**
   - Deteksi objek manusia dan mesin pada malam hari menggunakan kamera termal inframerah yang dipasang pada wahana tanpa awak (*drone*).
4. **Disertasi Batik Parallelogram (Dr. Jani Kusanti):**
   - Bimbingan doktoral Dr. Arief yang berhasil mempublikasikan 3 jurnal Scopus (*IJACSA, INASS*) dan mendemonstrasikan pengenalan motif batik secara real-time pada sidang terbuka promosi doktor.

---

## 5. 🗺️ Desain Roadmap Riset 5 Tahun (S3 & Hibah BIMA)

Dr. Arief membagikan formula menyusun peta jalan riset (*research roadmap*) bertahap selama 5 tahun agar tema disertasi selaras dengan skema pendanaan Hibah Nasional (Kemdiktisaintek BIMA):

```text
Tahun 1: Image Classification (Membedakan objek kelas A vs kelas B)
   │
   ▼
Tahun 2: Object Detection (Melokalisasi bounding box pada objek multi-skala)
   │
   ▼
Tahun 3: Fine-Grained Recognition & Severity Grading (Identifikasi spesifik & tingkat keparahan)
   │
   ▼
Tahun 4: Prototyping on Mobile/Edge Devices (Implementasi mandiri pada smartphone/IoT nir-server PC)
   │
   ▼
Tahun 5: Hilirisasi, Skalabilitas Sistem, & Uji Lapangan Industri / UMKM
```

---

## 6. ⚡ Konvergensi ke Kamera Tepi Otonom (*Autonomous Edge Vision*)

Perkembangan industri modern mengarah pada **pengurangan intervensi manusia (*minimal human intervention*)**:
* Kamera pengawas masa kini tidak lagi sekadar merekam secara pasif, melainkan harus mampu mengeksekusi inferensi kecerdasan buatan secara mandiri di tepi jaringan (*Autonomous Edge AI Camera*).
* Contoh implementasi: sistem *smart boarding gate* stasiun kereta api KAI yang mengenali biometrik wajah penumpang secara instan tanpa tiket fisik, serta kamera inspeksi K3 di kawasan industri.
* **Tantangan Rekayasa Perangkat Lunak:** Memampukan model komputasi visual (CNN/ViT) berjalan lancar pada perangkat berdaya rendah (*resource-constrained embedded devices*) dengan latensi rendah dan konsumsi memori SRAM minimal.

---
*Catatan kuliah ini disusun sebagai dokumentasi pembelajaran mandiri dan telaah akademis mata kuliah Visi Komputer Lanjut Program Doktor Ilmu Komputer UDINUS.*
