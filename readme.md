# Comparative Analysis of YOLOv8 and YOLO11 for Baggage Detection

Repositori ini berisi proyek implementasi dan analisis komparasi antara dua generasi algoritma Object Detection, yaitu **YOLOv8** dan **YOLO11**. Studi kasus yang diangkat adalah deteksi barang bawaan (**Backpack & Luggage**) untuk memenuhi tugas akhir / Penulisan Ilmiah di Universitas Gunadarma.

Aplikasi simulasi ini dilengkapi dengan antarmuka berbasis web menggunakan **Flask** untuk menguji performa akurasi dan kecepatan inferensi kedua model secara berdampingan (*side-by-side*).

## 📂 Struktur Proyek
```text
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
