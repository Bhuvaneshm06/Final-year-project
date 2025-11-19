# Final-year-project

# 🚨 Suspicious Activity Detection in CCTV using YOLOv8

An AI-powered intelligent surveillance system that detects suspicious human activities from CCTV footage using **YOLOv8 for pose estimation** and **XGBoost for behavior classification**.

---

## 📚 About the Project

This project aims to automate surveillance by identifying abnormal behaviors such as ** theft, violence**, etc., in real-time. It extracts human keypoints using YOLOv8 and classifies actions using an XGBoost model trained on pose features.

> 🔒 Real-time alerts and annotated videos help improve public safety while reducing manual monitoring overhead.

---

## 🧠 System Architecture

```
CCTV/Video → Frame Extraction → YOLOv8 Pose Estimation → Keypoint Feature Extraction → XGBoost Classification → Output + Alert
```

Annotated bounding boxes and confidence levels are overlaid on suspicious detections, with email alerts sent for high-confidence events.

---

## 🗂 Dataset: [DCSASS](https://www.kaggle.com/datasets/mateohervas/dcsass-dataset)

- Total Videos: 16,853
  - Normal: 9,676
  - Abnormal: 7,177
- Classes: 13 (Abuse, Arrest, Arson, Assault, Burglary, Explosion, etc.)
- Annotations: Bounding boxes + Labels

---

## 🛠️ Technologies Used

| Tool         | Purpose                                 |
|--------------|------------------------------------------|
| YOLOv8       | Pose estimation (17 body keypoints)      |
| XGBoost      | Behavior classification (Normal/Suspicious) |
| OpenCV       | Frame extraction, video processing       |
| Pandas/Numpy | Data transformation, keypoint handling   |
| Scikit-learn | Evaluation & Preprocessing               |
| Python       | Implementation language                  |

---

## ⚙️ Installation

```bash
git clone https://github.com/suspicious/suspicious-activity-detection.git
cd suspicious-activity-detection
pip install -r requirements.txt
```

**Recommended Environment:**  
Python 3.8+, 16GB RAM, GPU-enabled (for faster inference), Windows 11 / Linux

---

## 🚀 Usage

### ▶️ Run Detection

```bash
python src/suspicious.py --video path_to_video.mp4
```

### 📩 Send Email Alerts (for suspicious frames)

Alerts will be sent to registered security emails when confidence ≥ 85%.

---

## 🧪 Model Training

### 1. Frame Extraction

```bash
python src/suspicious.py
```

### 2. Feature Generation (YOLOv8 → Keypoints → CSV)

```bash
python src/suspicious.py
```

### 3. Train XGBoost Classifier

```bash
python src/train.py
```

### 4. Predict & Visualize

```bash
python src/suspicious.py --source test_video.mp4
```

---

## 📊 Results

| Metric     | Value |
|------------|-------|
| Accuracy   | 75%   |
| Precision  | High on Loitering & Theft |
| FPS        | 30+ (GPU) |

---

## 📦 Project Structure

```
📁 dataset/
📁 src/
    ├── train.py
    ├── suspicious.py
    ├── suspicious(frames).py
    ├── suspicious(extraction).py
📁 models/
📁 output/
README.md
requirements.txt
```

---

## 🔮 Future Enhancements

- Real-time live CCTV feed support
- Edge deployment (Jetson Nano, Raspberry Pi)
- Multi-class behavior classification (fight, theft, etc.)
- Use of 3D CNNs or Transformers for improved accuracy

---

## 👥 Authors

- Sagadevan D  
- Bhuvanesh M  
- Kuppusamy V  
- Mohamed Thowfic M  

**Institution:** Government College of Engineering, Dharmapuri  
**Supervisor:** Ms. M. Devi, Assistant Professor

---

## 📜 License

This project is licensed under the MIT License - Copyright (c) 2025 Sagadevan D, Bhuvanesh M, Kuppusamy V, Mohamed Thowfic M

---

## 📬 Contact

Security Email Alert Sender: **suspicious616@gmail.com**

