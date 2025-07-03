# Smart Eye Disease Detection using Deep Learning & Mobile Deployment

This project presents an end-to-end deep learning pipeline for early detection of eye diseases such as glaucoma, diabetic retinopathy, and cataracts. The system integrates advanced computer vision techniques with mobile-friendly deployment to facilitate accessible and accurate diagnosis.

## 🧠 Overview

Eye diseases are a leading cause of blindness, especially when left undiagnosed. This project leverages deep learning architectures like U-Net, autoencoders, and CNNs to analyze retinal images and predict disease conditions with high accuracy. Furthermore, the trained model is optimized for deployment on Android devices using TensorFlow Lite.

## 📁 Project Structure

```
eye disease/
├── data/                   # Contains preprocessed datasets and annotations
├── models/                 # Pre-trained and final model weights
├── src/                    # Source code for training, evaluation, and deployment
│   ├── segmentation/       # U-Net implementation for retinal vessel segmentation
│   ├── anomaly_detection/  # Autoencoder setup for detecting outliers
│   └── classification/     # CNNs for disease classification
├── tflite_model/           # TensorFlow Lite models and optimization scripts
├── mobile_app/             # Flutter or Android app integration code
└── README.md               # Project description
```

## 🛠️ Features

- 🧬 **Retinal Vessel Segmentation** using U-Net architecture.
- ⚠️ **Anomaly Detection** with autoencoders to filter poor-quality or anomalous images.
- 🩺 **Multi-Class Classification** of eye diseases using CNNs.
- 📲 **Mobile Deployment** using TensorFlow Lite for Android applications.
- 📊 Trained on popular ophthalmic datasets like:
  - **DRIVE**
  - **CHASE_DB1**
  - **IDRiD**
  - **e-Ophtha**

## 🏁 How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/eye-disease-detection.git
cd eye-disease-detection
```

### 2. Install Requirements

```bash
pip install -r requirements.txt
```

### 3. Train Models (Optional)

You can retrain models by navigating into respective subfolders in `src/`:

```bash
cd src/segmentation
python train_unet.py
```

### 4. Convert to TFLite

```bash
cd tflite_model
python convert_to_tflite.py
```

### 5. Deploy on Mobile

Follow the instructions inside `mobile_app/` to set up the Android application. The app can classify eye conditions directly from retinal images using the embedded model.

## 📈 Results

- **Segmentation Accuracy (IoU)**: ~0.87 on DRIVE
- **Classification Accuracy**: ~92.4% across 4 disease classes
- **Model Size after TFLite conversion**: ~5.6 MB
- **Average inference time**: ~200ms on mid-range Android devices

## 🧪 Demo

<p align="center">
  <img src="docs/demo1.gif" alt="Mobile App Demo" width="300"/>
  <img src="docs/demo2.gif" alt="Model Prediction" width="300"/>
</p>

## 📌 Future Work

- Include real-time capture and preprocessing via mobile camera.
- Expand dataset to include more rare eye conditions.
- Add explainable AI components to visualize model decision-making.

## 📄 License

This project is licensed under the MIT License.

## 🙋‍♂️ Authors

- **Kurma Koushik** – [GitHub](https://github.com/yourusername) · [LinkedIn](https://linkedin.com/in/yourprofile)
