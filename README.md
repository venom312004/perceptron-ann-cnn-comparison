# MNIST Digit Classification — Perceptron vs. ANN vs. CNN

A comparative study of three neural network architectures on the MNIST handwritten digit dataset, implemented with TensorFlow/Keras and scikit-learn.

---

## Overview

This project trains and evaluates three progressively complex models on the MNIST dataset — 70,000 grayscale images of handwritten digits (0–9) — to demonstrate how architecture complexity directly impacts classification accuracy.

| Model       | Architecture |
|-------------|--------------|
| Perceptron  | Flatten → Dense(10, softmax) |
| ANN         | Flatten → Dense(128, ReLU) → Dense(64, ReLU) → Dense(10, softmax) |
| CNN         | Conv2D → MaxPool → Conv2D → MaxPool → Flatten → Dense → Dropout(0.5) → Dense(10, softmax) |

---

## Project Structure
├── CNN.ipynb          # Main notebook: training, evaluation, and visualizations
├── mnist_train.csv    # Training data (60,000 samples)
└── mnist_test.csv     # Test data (10,000 samples)

---
---

## Tech Stack

- Python 3.x
- TensorFlow / Keras
- scikit-learn
- NumPy, Pandas
- Matplotlib, Seaborn

---

## Getting Started

1. Clone the repository and open `CNN.ipynb` in Jupyter or Google Colab.
2. Place `mnist_train.csv` and `mnist_test.csv` in the same directory (or upload when prompted in Colab).
3. Run all cells in order.

**Install dependencies (local only):**
```bash
pip install tensorflow scikit-learn pandas matplotlib seaborn
```

---

## Model Details

### Perceptron
- Single dense layer with softmax output
- Optimizer: SGD | Loss: Categorical Crossentropy

### ANN
- Two hidden layers with ReLU activation
- Optimizer: Adam | Loss: Categorical Crossentropy

### CNN
- Two Conv2D + MaxPooling blocks for spatial feature extraction
- Dropout (0.5) for regularization
- Optimizer: Adam | Loss: Categorical Crossentropy

---

## Results

All models trained for **5 epochs** on 60,000 training images and evaluated on 10,000 test images.

| Model      | Test Accuracy |
|------------|---------------|
| Perceptron | ~92%          |
| ANN        | ~97%          |
| CNN        | ~99%          |

The CNN outperforms both simpler architectures by leveraging convolutional filters to capture spatial patterns in image data.

---

## Visualizations

The notebook includes:
- Training and validation accuracy/loss curves for each model
- Side-by-side validation accuracy comparison across all three models
- Bar chart of final test accuracies
- Sample predictions on random test images

---

## Key Concepts

- Image preprocessing (normalization, reshaping)
- One-hot encoding with `to_categorical`
- Convolutional feature extraction (Conv2D + MaxPooling2D)
- Regularization via Dropout
- Multi-model comparison and evaluation

---

## License

This project is intended for educational purposes.
