# 🚗 Distracted Driver Detection Using Deep Learning

This project addresses the growing issue of distracted driving by developing and comparing deep learning models that classify driver behavior using dashboard camera images. Our goal is to detect potentially risky behaviors such as texting, drinking, or reaching behind while driving, enabling real-time interventions and contributing to safer roads.

---

## 🔬 Objectives

- Detect and classify driver actions based on dashboard camera images
- Evaluate baseline CNN performance against popular transfer learning models (MobileNet, VGG, ResNet)
- Improve road safety by identifying distractions that contribute to accidents

---

## 🧪 Dataset

We used the publicly available [State Farm Distracted Driver Detection dataset](https://www.kaggle.com/c/state-farm-distracted-driver-detection), which includes thousands of labeled images across 10 driver behavior classes:
- Safe driving
- Texting (right/left)
- Talking on phone (right/left)
- Operating radio
- Drinking
- Reaching behind
- Adjusting hair or makeup
- Talking to passengers

---

## 🧠 Methodology

- **Baseline CNN**: Four convolutional layers, batch normalization, ReLU, dropout, and fully connected layers
- **Transfer Learning**:
  - **MobileNet**: Lightweight model using depthwise separable convolutions
  - **VGG16**: Deep CNN with standard 3x3 filters
  - **ResNet50**: Deep residual network using skip connections
- Used early stopping, dropout, and batch normalization to improve generalization
- Trained using TensorFlow on M1 Mac GPU with transfer learning for pretrained models

---

## 📈 Results

| Model      | Test Accuracy |
|------------|----------------|
| CNN (Baseline) | 96.66%         |
| MobileNet      | 94.38%         |
| VGG16          | **98.17%**     |
| ResNet50       | 21.45%         |

- VGG outperformed all models with highest accuracy
- MobileNet offered fast inference, making it suitable for real-time applications
- ResNet underperformed likely due to overfitting or training constraints

---

## 📌 Technologies Used

- Python
- TensorFlow & Keras
- NumPy, Pandas, Matplotlib
- Transfer Learning (ImageNet weights)
- Dashboard camera imagery dataset from Kaggle

---

## 📄 Reports

- [📓 Final Report (DOCX)](reports/Final_Report_distracted_driver_detection.docx)
- [📊 Project Presentation (PPTX)](reports/DRIVER%20ACTION%20DETECTION.pptx)

---

## 📃 License

This project is licensed under the [MIT License](LICENSE).
