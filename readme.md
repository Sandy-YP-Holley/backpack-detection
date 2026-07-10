# Comparative Analysis of YOLOv8 and YOLO11 for Baggage Detection

Repositori ini berisi proyek implementasi dan analisis komparasi antara dua generasi algoritma Object Detection, yaitu **YOLOv8** dan **YOLO11**. Studi kasus yang diangkat adalah deteksi barang bawaan (**Backpack & Luggage**) untuk memenuhi tugas akhir / Penulisan Ilmiah di Universitas Gunadarma.

Aplikasi simulasi ini dilengkapi dengan antarmuka berbasis web menggunakan **Flask** untuk menguji performa akurasi dan kecepatan inferensi kedua model secara berdampingan (*side-by-side*).

## 📂 Struktur Proyek
baggage-detection-yolo-comparison/
├── app.py                      # Backend web Flask untuk simulasi komparasi
├── best_yolov8_final.pt        # Bobot model final YOLOv8 (963 citra, 50 epoch)
├── best_yolov11_final.pt       # Bobot model final YOLO11 (963 citra, 50 epoch)
├── dataset/                    # Dataset baseline awal (200 citra)
├── dataset_baru/               # Dataset upgrade (963 citra)
├── runs/                       # Grafik hasil training, metrik, & confusion matrix dari Colab
├── templates/
│   └── index.html              # Antarmuka UI web simulasi
├── static/
│   └── uploads/                # Direktori penyimpanan sementara foto uji
└── *.ipynb                     # File notebook runtime Google Colab asli

### 📊 Hasil Eksperimen & Metrik EvaluasiPengujian dilakukan secara adil (fair comparison) melalui dua tahap: Tahap Baseline (200 citra, 20 epoch) dan Tahap Upgrade Fine-Tuning (963 citra, 50 epoch). Berikut adalah rekapitulasi data performa kedua model:Arsitektur ModelDatasetEpochPrecisionRecallmAP50Waktu Inferensi (CPU)YOLOv8 (Baseline)200 Citra2065.6%47.6%54.8%~3.2 msYOLO11 (Baseline)200 Citra2071.1%42.7%51.4%~4.1 msYOLOv8 (Final)963 Citra5099.5%99.9%99.0%~3.6 msYOLO11 (Final)963 Citra5098.5%99.8%99.4%~5.2 msAnalisis Singkat untuk Sidang:Peningkatan Skala Data: Penambahan data dari 200 menjadi 963 citra (melalui teknik augmentasi Roboflow) terbukti mendongkrak nilai akurasi (mAP50) kedua model dari kisaran 50% menjadi 99%.Komparasi Model Final: YOLOv8 unggul sangat tipis pada nilai kedekatan tebakan (Precision 99.5%) dan kecepatan komputasi. Namun, YOLO11 terbukti memiliki arsitektur yang lebih stabil dalam mengenali batas objek spasial (mAP50 99.4%) serta lebih kebal terhadap masalah False Positive (halusinasi objek latar belakang).

### 🛠️ Cara Menjalankan Aplikasi di Lokal (Laptop)
1. Clone Repositori : git clone [https://github.com/Sandy-YP-Holley/baggage-detection-yolo-comparison.git](https://github.com/Sandy-YP-Holley/baggage-detection-yolo-comparison.git)
cd baggage-detection-yolo-comparison
2. Install Dependencies : Pastikan Python sudah terpasang di sistem Anda, lalu install pustaka yang dibutuhkan: pip install flask ultralytics torch torchvision
3. Jalankan Server Flask python app.py
Setelah server menyala, buka peramban (browser) Anda lalu akses alamat: http://127.0.0.1:5000 atau http://localhost:5000.
