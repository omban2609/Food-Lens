# 🍕 FoodLens — AI Food Image Classifier

> A computer vision web app that identifies food from photos or live webcam, running entirely in the browser with no backend required.

![FoodLens Demo](screenshot.png)

---

## 🧠 What I Built

FoodLens is an end-to-end machine learning project — from training a deep learning model to deploying it as a live web app. Upload any food photo or point your webcam at food, and the AI instantly classifies it with confidence scores.

**Supported food categories:**
- 🍕 Pizza
- 🍔 Hamburger
- 🍣 Sushi
- 🍦 Ice Cream
- 🍚 Fried Rice

---

## ✨ Features

- 📸 Upload image or use live webcam
- ⚡ Real-time inference — no server, runs fully in the browser
- 📊 Confidence score bars for all 5 categories
- 🎯 ~95% validation accuracy
- 📱 Responsive design — works on mobile too

---

## 🔬 How It Works

### 1. Model Training (Google Colab)
- Used the **Food-101 dataset** — a real-world dataset with 101,000 food images
- Applied **Transfer Learning** with **MobileNetV2** pretrained on ImageNet
- Froze the base model and added custom classification layers on top
- Trained for 7 epochs with early stopping — achieved **95.68% validation accuracy**
- Exported using **TensorFlow.js converter** for browser inference

### 2. Browser Inference (TensorFlow.js)
- Model runs entirely client-side using **TensorFlow.js**
- Images are resized to 224×224 and normalized before inference
- No data ever leaves the user's device

### 3. Frontend
- Built with **vanilla HTML, CSS, and JavaScript** — no frameworks
- Drag & drop or click to upload images
- Webcam support with live capture

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Model Training | Python, TensorFlow, Keras |
| Dataset | Food-101 (TensorFlow Datasets) |
| Transfer Learning | MobileNetV2 (ImageNet weights) |
| Model Export | TensorFlow.js Converter |
| Browser Inference | TensorFlow.js |
| Frontend | HTML, CSS, JavaScript |
| Deployment | GitHub Pages |
| Training Environment | Google Colab (free GPU) |

---

## 📈 Training Results

| Metric | Value |
|---|---|
| Training Accuracy | 98.4% |
| Validation Accuracy | 95.68% |
| Epochs Trained | 7 (early stopping) |
| Base Model | MobileNetV2 |
| Dataset | Food-101 (5 classes) |

---

## 🚀 Run Locally
```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/FoodLens.git
cd FoodLens

# Serve locally (model files need HTTP to load)
npx serve .
```

Then open `http://localhost:3000` in your browser.

---

## 🌐 Live Demo

**[Try it live →](https://YOUR_USERNAME.github.io/FoodLens)**

---

## 📚 What I Learned

- How **transfer learning** works and why it's powerful for small datasets
- How to build and train a **custom image classifier** in TensorFlow/Keras
- How to export a trained model to **TensorFlow.js** for browser inference
- How to handle **dataset filtering, preprocessing, and label remapping**
- End-to-end ML pipeline: data → training → export → deployment

---

## 📁 Project Structure
```
FoodLens/
├── index.html          # Full frontend app
├── model.json          # TF.js model architecture
├── group1-shard1of3.bin  # Model weights (part 1)
├── group1-shard2of3.bin  # Model weights (part 2)
├── group1-shard3of3.bin  # Model weights (part 3)
└── screenshot.png      # App screenshot
```

---

*Built with TensorFlow.js — no backend, no API calls, just pure in-browser AI.*
