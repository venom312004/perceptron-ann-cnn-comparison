🔢 MNIST Digit Classification — Perceptron vs ANN vs CNN
A comparative study of three neural network architectures on the classic MNIST handwritten digit dataset, built with TensorFlow/Keras and scikit-learn.

📌 Overview
This project trains and evaluates three models on the MNIST dataset (70,000 grayscale images of handwritten digits, 0–9):
ModelArchitecturePerceptronFlatten → Dense(10, softmax)ANNFlatten → Dense(128) → Dense(64) → Dense(10, softmax)CNNConv2D → MaxPool → Conv2D → MaxPool → Flatten → Dense → Dropout → Dense(10, softmax)
The goal is to show how model complexity directly impacts classification accuracy.

🗂️ Project Structure
CNN.ipynb          # Main notebook with all models, training, and visualizations
mnist_train.csv    # Training data (60,000 samples)
mnist_test.csv     # Test data (10,000 samples)

⚙️ Tech Stack

Python 3.x
TensorFlow / Keras
scikit-learn
NumPy, Pandas
Matplotlib, Seaborn


🚀 How to Run

Clone the repo and open CNN.ipynb in Google Colab or Jupyter.
Upload mnist_train.csv and mnist_test.csv when prompted (or place them in the same directory).
Run all cells in order.

bash# Install dependencies if running locally
pip install tensorflow scikit-learn pandas matplotlib seaborn

🧠 Model Details
Perceptron

Single dense layer with softmax output
Optimizer: SGD | Loss: Categorical Crossentropy

ANN (Artificial Neural Network)

Two hidden layers (ReLU activation)
Optimizer: Adam | Loss: Categorical Crossentropy

CNN (Convolutional Neural Network)

Two Conv2D + MaxPooling blocks for feature extraction
Dropout (0.5) to prevent overfitting
Optimizer: Adam | Loss: Categorical Crossentropy


📊 Results
All models trained for 5 epochs on 60,000 images, evaluated on 10,000 test images.
ModelTest AccuracyPerceptron~92%ANN~97%CNN~99%

CNN outperforms both Perceptron and ANN due to its ability to capture spatial features in images through convolutional filters.


📈 Visualizations
The notebook includes:

Training & validation accuracy/loss curves per model
Side-by-side validation accuracy comparison across all three models
Bar chart of final test accuracies
Sample predictions on random test images


📚 Key Concepts Demonstrated

Image preprocessing (normalization, reshaping)
One-hot encoding with to_categorical
Convolutional feature extraction (Conv2D + MaxPooling2D)
Regularization via Dropout
Multi-model comparison and evaluation


📝 License
This project is for educational purposes.
