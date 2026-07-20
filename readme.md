# 🎒 Comparative Analysis of YOLOv8 and YOLO11 for Baggage Detection

A computer vision project comparing the performance of **YOLOv8** and **YOLO11** for detecting baggage objects (backpacks and luggage).

Developed as an undergraduate research project at **Gunadarma University**, this application provides a web-based interface for comparing both models side-by-side while evaluating their accuracy and inference speed.

---

## ✨ Features

- 🔍 Detect backpacks and luggage from uploaded images
- ⚖️ Side-by-side comparison between YOLOv8 and YOLO11
- 📈 Performance evaluation using Precision, Recall, mAP50, and inference time
- 🌐 Flask web interface
- 📊 Includes training metrics, confusion matrices, and experiment results

---

## 🛠️ Technologies

- Python
- Flask
- Ultralytics YOLO
- PyTorch
- OpenCV
- HTML
- CSS

---

## 📂 Project Structure

```
baggage-detection-yolo-comparison/
│
├── app.py
├── templates/
├── static/
├── dataset/
├── dataset_baru/
├── runs/
├── best_yolov8_final.pt
├── best_yolov11_final.pt
└── notebooks/
```

---

## 📊 Experimental Results

| Model | Dataset | Precision | Recall | mAP50 | Inference |
|-------|---------|----------:|--------:|-------:|----------:|
| YOLOv8 | 200 Images | 65.6% | 47.6% | 54.8% | ~3.2 ms |
| YOLO11 | 200 Images | 71.1% | 42.7% | 51.4% | ~4.1 ms |
| YOLOv8 | 963 Images | **99.5%** | **99.9%** | 99.0% | **~3.6 ms** |
| YOLO11 | 963 Images | 98.5% | 99.8% | **99.4%** | ~5.2 ms |

---

## 📈 Key Findings

- Increasing the dataset from **200** to **963 images** significantly improved model performance.
- YOLOv8 achieved slightly better precision and faster inference.
- YOLO11 achieved slightly higher mAP50, indicating more consistent localization performance.
- Both models exceeded **99% detection accuracy** after fine-tuning.

---

## 🚀 Installation

Clone the repository

```bash
https://github.com/Sandy-YP-Holley/backpack-detection.git
```

Install dependencies

```bash
pip install flask ultralytics torch torchvision
```

Run the application

```bash
python app.py
```

Open

```
http://localhost:5000
```

---

## 🎓 Purpose

This project was developed as part of an undergraduate research project to compare two generations of YOLO object detection models using identical datasets and evaluation metrics.

---

## 📄 License

Licensed under the MIT License.

---

## 👨‍💻 Author

**Sandy Yoga Prakasa Holley**

GitHub:
https://github.com/Sandy-YP-Holley
