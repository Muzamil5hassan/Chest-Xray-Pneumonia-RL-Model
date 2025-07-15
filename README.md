
#  Pneumonia Detection by Reinforcement Learning with CNN

This project implements an AI system to detect **pneumonia** in chest X-ray images by combining **Convolutional Neural Networks (CNNs)** with **Reinforcement Learning (RL)** to optimize training.

---

## Features
- Classifies chest X-ray images as **pneumonia** or **normal**
- Uses custom **Gym environment** for RL-based training
- Image preprocessing with resizing and normalization
- Model built with **TensorFlow / Keras**
- Final trained model can be used to predict new images

---

##  Model Overview

- **Input size:** 150×150 grayscale images

- **CNN architecture:**

- Conv2D → Conv2D → BatchNormalization → MaxPooling → Dropout
- Flatten → Dense → Dropout → Dense (output)


- **Output:** 2 classes (pneumonia / normal)

- **Reinforcement Learning:**
- Custom environment (`Env4RLClassification`)
- Exploration-exploitation balance with ε-decay
- Reward based on correct predictions
- Updates Q-values during episodes to guide learning

---

## ▶️ How to Use

**Preprocessing:**
- Resize images to 150×150
- Convert to grayscale
- Normalize pixel values (0–1)

**Train the model:**
- Run the main Python script (`final_year_code_from_111.py`)
- Model trains for `num_episodes` episodes using RL
- Trained model saved as `.keras` file

**Predict a single image:**
```python
predicted_label = predict_image(model, '/path/to/image.jpg', image_size=150)
print(f"The model predicts this image is: {predicted_label}")
```

# Dependencies
Python ≥ 3.7

TensorFlow

Keras

OpenCV

NumPy

Pandas

Gym / Gymnasium

Matplotlib

All dependencies can be installed via pip.

# Results
The model was trained over multiple episodes using RL

Achieves balanced accuracy by exploring and optimizing classification policy

# Output
Trained model saved as:
```python
24-4modelChest20.keras
```
# Author

Muzamil Hassan Magsi

Bachelor of Science in Computer Systems Engineering

Islamia University of Bahawalpur

 Feel free to ask if you'd like me to add installation instructions, a license, sample training graphs, or a Colab badge!
If you'd like, I can also create a version with badges and a preview image, or export it as a ready-to-use file.  
Let me know!
