# 📌 Catatan Perkuliahan: Penambangan Data Lanjut (Pertemuan 1)
**Mata Kuliah:** Advanced Data Mining (Penambangan Data Lanjut)  
**Dosen Pengampu:** Prof. Ir. Heru Agus Santoso, Ph.D., IPM., ASEAN Eng. (Dosen PDIK UDINUS)  
**Program:** Program Doktor Ilmu Komputer (PDIK) - Universitas Dian Nuswantoro (UDINUS)  
**Semester:** Gasal 2026/2027  

---

## 🧭 Pendahuluan & Orientasi Perkuliahan

Mata kuliah **Penambangan Data Lanjut (*Advanced Data Mining*)** pada Program Doktor Ilmu Komputer (PDIK) UDINUS diampu oleh **Prof. Ir. Heru Agus Santoso, Ph.D., IPM., ASEAN Eng.**. Perkuliahan ini membedah paradigma baru penambangan data tingkat doktoral (S3): beranjak dari pemahaman prosedural konvensional sarjana menuju **isu kebaruan metodologis (*methodological novelty*)** yang sedang berkembang pesat pada publikasi konferensi internasional dan jurnal bereputasi tinggi.

### A. Filosofi Doktoral & Urgensi Perencanaan Publikasi Sejak Dini
* **Target Utama:** Kelulusan tepat waktu (*on-time graduation*).
* **Prinsip Riset Doktoral:** Seluruh mahasiswa S3 diasumsikan telah menguasai konsep dasar *data mining*. Oleh karena itu, perkuliahan langsung diarahkan pada identifikasi celah riset (*research gap*) dari literatur mutakhir.
* **Hakikat Riset (*Re-Search*):** Riset ilmiah adalah meneliti kembali apa yang telah ditemukan peneliti terdahulu guna melahirkan perbaikan atau kebaruan metode. Tidak ada riset yang berdiri terisolasi tanpa korelasi literatur.

### B. Dekonstruksi RPS: Meninggalkan CRISP-DM Konvensional
* Pada jenjang sarjana (S1), proses penambangan data diajarkan menggunakan kerangka **CRISP-DM (*Cross-Industry Standard Process for Data Mining*)**: *Business Understanding, Data Understanding, Data Preparation, Modeling, Evaluation, Deployment*.
* Prof. Heru menegaskan bahwa di level S3, pengulangan teori CRISP-DM standar tidak lagi relevan. Mahasiswa doktoral harus langsung membedah **delapan pilar advance data mining kontemporer** yang menjadi topik utama di komunitas ilmiah global.

### C. Kerangka Penyelidikan Doktoral (Inquiry Triangle & Research Mapping)
Prof. Heru menekankan bahwa mahasiswa S3 tidak boleh terburu-buru menulis kode program (*"jangan langsung coding dulu, pelan-pelan pahami teorinya"*). Mahasiswa harus melalui tiga tahapan eksplorasi:
1. **What:** Memahami hakikat definisi, teori dasar, dan formulasi matematis metode.
2. **Why:** Menemukan alasan mengapa teknik tersebut dipilih dan kelemahan apa dari metode terdahulu yang diperbaiki.
3. **Outcome / Benefit:** Mengukur dampak kebaruan (*novelty*) dan manfaat nyata yang dihasilkan bagi keilmuan dan masyarakat.
4. **Pemetaan Posisi Riset (*Research Coverage*):** Peneliti harus mampu memetakan letak risetnya pada pohon taksonomi keilmuan (contoh pada *Uncertain Graph Mining*: apakah berada di ranah *Query Problems, Computational Problems,* atau *Algorithmic Problems*).

---

## 1. 🧱 Delapan Pilar Advance Data Mining Kontemporer

Prof. Heru Agus Santoso mengelompokkan spektrum riset data mining modern ke dalam 8 pilar utama:

```
                  ┌─────────────────────────────────────────────────────────────┐
                  │       ADVANCED DATA MINING TAXONOMY (PROF. HERU SANTOSO)    │
                  └──────────────────────────────┬──────────────────────────────┘
                                                 │
         ┌───────────────────────────────┬───────┴───────┬───────────────────────────────┐
         ▼                               ▼               ▼                               ▼
┌──────────────────┐            ┌──────────────────┐   ┌──────────────────┐    ┌──────────────────┐
│ MULTIMODAL & RAG │            │ EXPLAINABLE (XAI)│   │  FAIRNESS & PPDM │    │ SPATIO-TEMPORAL  │
├──────────────────┤            ├──────────────────┤   ├──────────────────┤    ├──────────────────┤
│• Tabular + Text  │            │• SHAP & LIME     │   │• Bias Mitigation │    │• Time Series LSTM│
│  + Image Fusion  │──────────► │• Black-Box Proof │──►│• Federated Learn.│───►│• Spatial CNN Loc.│
│• RAG via LLMs    │            │• WHO Standard    │   │• Zero Raw Sharing│    │• Concept Drift   │
│• FP-Growth Rules │            │  Justification   │   │  (Privacy Bounds)│    │• IoT Screening   │
└──────────────────┘            └──────────────────┘   └──────────────────┘    └──────────────────┘
```

---

### A. Multimodal Data Mining & Cross-Modal Pattern Mining
* **Karakteristik Masalah:** Data di dunia nyata bersifat heterogen. Contoh pada rekam medis: data tabular (hasil tes lab numerik), data teks narasi (catatan klinis dokter), dan data citra (radiologi MRI/CT-scan).
* **Fusi Fitur (*Feature Fusion*):**
  - Mengintegrasikan berbagai modalitas ke dalam satu ruang representasi vektor bersama (*unified feature space*).
  - Teks diekstraksi menggunakan *text embedding*, citra diekstraksi via *convolutional/vision transformer features*, dan data tabular dinormalisasi.
* **Penambangan Pola & Fenotipe Penyakit:**
  - Data kontinu diubah menjadi kategorikal (*discretization*).
  - Algoritma **FP-Growth (*Frequent Pattern Growth*)** diterapkan untuk mengekstraksi aturan asosiasi lintas-modalitas (*cross-modal association rules*) berbasis metrik *Support, Confidence, dan Lift Ratio*.
  - Menghasilkan identifikasi **Fenotipe Penyakit (*Disease Phenotype*)**, yaitu pola tanda fisik klinis nyata akibat interaksi faktor genetik dan lingkungan.

---

### B. Text-Guided Data Mining & Retrieval-Augmented Generation (RAG)
* **Konsep:** Memanfaatkan model bahasa besar (*Large Language Models / LLM*) seperti Llama atau GPT dengan teknik *Retrieval-Augmented Generation (RAG)* untuk memperkaya (*enrichment*) data tidak terstruktur sebelum proses pemodelan.
* **Kasus Medis:** Kode penyakit ICD (*International Classification of Diseases*) yang tertera pada basis data diperkaya secara otomatis dengan informasi nutrisi, pola hidup (*habit*), dan literatur patofisiologi terkini.
* **Pembeda Riset S3:** Kebaruan ilmiah bukan sekadar mengunggah tabel ke ChatGPT, melainkan meneliti **efisiensi arsitektur penarikan informasi (RAG)** agar pengayaan data tersebut terbukti signifikan mendongkrak akurasi algoritma *downstream* konvensional (SVM, Random Forest, XGBoost).

---

### C. Explainable AI (XAI) & Pembuktian Berstandar Internasional
* **Tantangan Kotak Hitam (*Black Box*):** Algoritma deep learning memiliki akurasi tinggi namun tidak transparan. Praktisi klinis dan industri menolak mengadopsi model tanpa pemahaman alasan logis di balik keputusannya.
* **Metode Utama:** **SHAP (*SHapley Additive exPlanations*)**, **LIME**, **Grad-CAM**, dan *Counterfactual Explanations*.
* **Studi Kasus Jurnal Elsevier (Prof. Heru dkk., 2025):**
  - **Artikel Ilmiah:** *"Enhancing nutritional status prediction through attention-based deep learning and explainable AI"* (Jurnal *Intelligence-Based Medicine*, Elsevier, Vol. 11, 2025).
  - Prediksi status gizi balita (*undernutrition/stunting*).
  - Menerapkan SHAP untuk mengekstraksi variabel paling berpengaruh terhadap stunting.
  - **Kunci Publikasi Internasional:** Menyelaraskan hasil matematis SHAP dengan **standar internasional WHO (*World Health Organization*)**. Terbukti bahwa balita stunting variabel paling determinan adalah **tinggi badan (kerdil)**, bukan berat badan. Bayi kurus masih dapat dipulihkan dengan nutrisi jangka pendek, namun keterlambatan tinggi badan membuktikan gangguan pertumbuhan kronis jangka panjang. Penyelarasan matematis XAI dengan standar internasional inilah yang melahirkan publikasi jurnal bereputasi tinggi.

---

### D. Causal Data Mining & Causal Discovery
* Memisahkan secara tegas antara **korelasi murni (*spurious correlation*)** dengan **hubungan sebab-akibat (*causality*)**.
* Melalui *causal discovery*, penambangan data mampu menghasilkan aturan kausalitas (*causal rules*) yang kokoh sebagai landasan sistem pendukung keputusan (*decision support systems*).

---

### E. Fairness-Aware Data Mining & Eliminasi Bias
* **Prinsip Keadilan:** Memastikan model penambangan data bebas dari bias sistemik terhadap atribut sensitif: **jenis kelamin (gender), ras, warna kulit, dan status sosio-ekonomi**.
* **Uji Generalisasi:** Model yang dilatih pada populasi tertentu (misal: Indonesia) harus tetap adil dan akurat saat diuji pada populasi demografi berbeda (Timur Tengah, Afrika, atau negara maju).
* **Pengalaman Empiris Publikasi Q1 Prof. Heru:** Riset *Visually Impaired Masseur Assistance Application (VIMAA)* di jurnal bereputasi tinggi **Q1 (*Assistive Technology*, Taylor & Francis)** bersama peneliti Universitas Diponegoro (UNDIP) dan Pertuni Kota Semarang. Reviewer internasional sangat ketat mengaudit potensi diskriminasi algoritmik terkait variabel gender dan identitas komunitas, sehingga menuntut justifikasi keadilan data secara transparan (*fairness-aware machine learning*).

---

### F. Graph Mining & Graph Neural Networks (GNN)
* **Karakteristik Data Graf:** Memodelkan relasi jaringan non-linier yang kompleks.
* **Evolusi Keilmuan:** Transisi dari pendekatan ontologi semantik klasik menuju **Graph Neural Networks (GNN)**, mekanisme atensi graf (*Graph Attention Networks*), dan *Graph Transformers*.
* **Graf Dinamis & Temporal (*Temporal Graph Mining*):** Menambang pola jaringan yang strukturnya terus berubah seiring waktu (contoh: rantai penularan penyakit pandemi, deteksi bot vs manusia pada kampanye hitam digital, serta pelacakan transaksi pencucian uang / *financial fraud*).

---

### G. Privacy-Preserving Data Mining (PPDM) & Federated Learning
* **Dilema Silo Data:** Basis data rekam medis di berbagai rumah sakit terisolasi dan tidak boleh disatukan secara terpusat karena terikat regulasi privasi (HIPAA / UU Perlindungan Data Pribadi).
* **Solusi Federated Learning:**
  - Algoritma bergerak mendatangi data di perangkat/server lokal masing-masing institusi.
  - Pelatihan dilakukan secara lokal; hanya vektor pembaruan bobot model (*gradient updates*) yang dikirimkan ke server agregasi pusat.
  - Menjamin **nol transmisi data mentah (*zero raw data sharing*)** dengan tetap menghasilkan model global yang akurat.

---

### H. Spatio-Temporal, Streaming Data Mining & Concept Drift
* **Konvergensi Waktu & Ruang:** Mengombinasikan model sekuensial waktu **LSTM** dengan model spasial lokasi **CNN**.
* **Studi Kasus Sensor IoT Screening Kesehatan (Hibah BRIN/LPDP Prof. Heru):**
  - Mengembangkan perangkat **Anjungan Kesehatan Mandiri** berbasis sensor IoT bersama Dinas Kesehatan Kota Semarang.
  - Melakukan *rapid screening* antropometri, gula darah, asam urat, dan kolesterol di Puskesmas perkotaan secara berkala.
  - Data sekuensial (temporal) dipadukan dengan koordinat spasial untuk memetakan klaster persebaran penderita gula darah tinggi secara *real-time*.
* **Fenomena Pergeseran Konsep (*Concept Drift*):**
  - Pola masa lalu tiba-tiba bergeser maknanya di masa depan seiring waktu.
  - **Analogi Konsep OOP Prof. Heru:**
    * *Concept* diibaratkan sebagai *Class* (wadah/ember).
    * *Data* diibaratkan sebagai *Instance* (air di dalam ember).
    * Jika instance di dalam wadah berubah, maka konsep maknanya mengalami pergeseran (*drift*).
  - *Contoh:* Kata *"Apple"* dahulu dipahami murni sebagai buah, kini dominan merujuk pada gawai teknologi. Pada analisis ujaran kebencian (*hate speech*), kata slang di kalangan generasi muda dapat bergeser dari umpatan kasar menjadi ungkapan kekaguman (*"anjir keren banget"*).

---

## 2. 🧭 Distingsi Metodologis: Terstruktur vs Tidak Terstruktur

Dalam sesi tanya jawab mengenai deteksi disinformasi/hoaks, Prof. Heru memberikan panduan metodologis kritis:

```text
┌─────────────────────────────────────────────────────────────────────────────┐
│             DISTINGSI METODOLOGIS: TERSTRUKTUR VS TIDAK TERSTRUKTUR         │
├───────────────────────────────┬─────────────────────────────────────────────┤
│ Karakteristik Masalah         │ Pendekatan Komputasi yang Tepat             │
├───────────────────────────────┼─────────────────────────────────────────────┤
│ MASALAH TERSTRUKTUR           │ DATABASE QUERY (Bukan Riset Data Mining S3) │
│ • Validasi fakta deterministik│ • Pencocokan langsung tanggal/waktu pada    │
│ • Nilai biner absolut (0 vs 1)│   basis data resmi (contoh: Database BNPB). │
│ • Tidak ada ketidakpastian    │ • Selesai dengan kueri SQL / API lookup.    │
├───────────────────────────────┼─────────────────────────────────────────────┤
│ MASALAH TIDAK TERSTRUKTUR     │ ADVANCED DATA MINING (Layak Disertasi S3)   │
│ • Narasi teks bebas & ambigu  │ • Probabilistic Modeling (P = 0.79).        │
│ • Terdapat ketidakpastian     │ • Named Entity Recognition (NER).           │
│ • Multi-modal (Teks + Citra)  │ • Feature Selection + XAI (SHAP/LIME).      │
└───────────────────────────────┴─────────────────────────────────────────────┘
```

1. **Kasus Terstruktur:** Jika verifikasi hoaks hanya menguji kecocokan tanggal berita dengan data historis instansi resmi (misal: BNPB), masalah tersebut cukup diselesaikan dengan **Database Query** biasa dan tidak memenuhi standar kebaruan disertasi doktor.
2. **Kasus Tidak Terstruktur:** Penambangan data diperlukan saat menghadapi **ketidakpastian (*uncertainty*)** pada teks narasi bebas, di mana model menghasilkan estimasi probabilitas anomali informasi.
3. **Penerapan XAI pada Teks:**
   - XAI relevan jika model yang digunakan tergolong *black box* (Bi-LSTM / Deep Transformer).
   - Pada teks, setiap kata adalah sebuah fitur (*every single word is a feature*). Mahasiswa **wajib melakukan reduksi dimensi (*dimensionality reduction*)** terlebih dahulu sebelum menerapkan SHAP/LIME agar visualisasi atribusi kata ringkas dan dapat diinterpretasikan secara ilmiah.

---

## 3. 🧪 Implementasi Hands-On Python: Fusi Multimodal ($100 \times 2435$) & FP-Growth

Untuk mereproduksi secara konkret demonstrasi perkuliahan Prof. Ir. Heru Agus Santoso, repositori ini menyertakan skrip Python mandiri yang dapat langsung dijalankan:
* **Berkas Skrip:** [`simulasi_hands_on_multimodal_mining.py`](./simulasi_hands_on_multimodal_mining.py)

### Tahapan Pipeline Eksperimen:
1. **Sintesis Data Pasien (100 Pasien $\times$ 2.435 Fitur):**
   - Modality 1: Tabular Lab Scale (35 fitur numerik: tekanan darah, gula darah, BMI).
   - Modality 2: Teks Narasi Klinis Dokter (400 dimensi vektor semantik gejala).
   - Modality 3: Citra Medis Radiologi (2.000 dimensi fitur konvolusional).
2. **Cross-Modal Feature Fusion:**
   - Penggabungan horizontal menjadi matriks berdimensi $100 \times 2435$ (*Unified Feature Space*).
3. **Klasterisasi K-Means ($k=3$):**
   - Menghasilkan sebaran pasien yang persis sama dengan perkuliahan:
     * **Klaster 0:** 27 pasien ($27\%$) $\rightarrow$ Sub-kelompok berisiko (*pre-hipertensi*).
     * **Klaster 1:** 47 pasien ($47\%$) $\rightarrow$ Kelompok mayoritas (*penderita hipertensi akut*).
     * **Klaster 2:** 26 pasien ($26\%$) $\rightarrow$ Kelompok sehat (*normal*).
4. **Diskretisasi & Aturan Asosiasi FP-Growth:**
   - Transformasi fitur kontinu menjadi item kategorikal.
   - Menghasilkan aturan asosiasi lintas-modalitas (*cross-modal rules*) untuk mengekstraksi **Disease Phenotype** (fenotipe penyakit) berbasis metrik *Support, Confidence, dan Lift Ratio*.

```bash
# Menjalankan skrip simulasi langsung di terminal:
python simulasi_hands_on_multimodal_mining.py
```

---
*Catatan perkuliahan ini disusun sebagai dokumentasi pembelajaran mandiri dan telaah akademis mata kuliah Penambangan Data Lanjut Program Doktor Ilmu Komputer UDINUS.*
