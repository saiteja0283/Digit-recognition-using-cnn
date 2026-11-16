# Handwritten Digit Recognition Using CNN

## 📌 Project Overview

Handwritten Digit Recognition Using Convolutional Neural Networks (CNN) is a deep learning project that identifies handwritten digits from images.

This project uses the **MNIST dataset**, which contains handwritten digits from 0 to 9. A CNN model is trained to recognize these digits and predict the correct digit from a given handwritten image.

The project is implemented using Python and TensorFlow/Keras in a Jupyter Notebook.

## 🎯 Objectives

- To recognize handwritten digits automatically.
- To understand and implement Convolutional Neural Networks.
- To train a deep learning model using the MNIST dataset.
- To predict digits from uploaded handwritten images.
- To evaluate the model using accuracy and loss.

## 📂 Dataset

The project uses the **MNIST dataset**.

- Training images: 60,000
- Testing images: 10,000
- Image size: 28 × 28 pixels
- Image format: Grayscale
- Number of classes: 10 (digits 0–9)

The pixel values are normalized from the range 0–255 to 0–1 before training.

## 🛠️ Technologies Used

- Python
- TensorFlow and Keras
- NumPy
- Matplotlib
- Pillow (PIL)
- Jupyter Notebook
- ipywidgets

## 🧠 CNN Model Architecture

The project uses the following CNN architecture:

1. **Input Layer:** Accepts 28 × 28 grayscale images.
2. **Convolutional Layer 1:** Uses 32 filters with a 3 × 3 kernel and ReLU activation.
3. **Max Pooling Layer 1:** Reduces the spatial dimensions.
4. **Convolutional Layer 2:** Uses 64 filters with a 3 × 3 kernel and ReLU activation.
5. **Max Pooling Layer 2:** Further reduces the image dimensions.
6. **Flatten Layer:** Converts feature maps into a one-dimensional vector.
7. **Dense Layer:** Contains 128 neurons with ReLU activation.
8. **Dropout Layer:** Reduces overfitting by randomly disabling some neurons during training.
9. **Output Layer:** Contains 10 neurons with Softmax activation to predict digits from 0 to 9.

## ⚙️ Project Workflow

1. Import the required Python libraries.
2. Load the MNIST dataset.
3. Visualize sample handwritten digit images.
4. Normalize and reshape the images.
5. Build the CNN model.
6. Compile the model using the Adam optimizer and sparse categorical crossentropy loss.
7. Train the model using the training dataset.
8. Validate and evaluate the model.
9. Visualize training accuracy and loss.
10. Predict digits from test images and uploaded handwritten images.
11. Save the trained model.

## 📦 Installation

Install the required libraries using the following command:

```bash
pip install tensorflow numpy matplotlib pillow ipywidgets jupyter
```

## ▶️ How to Run the Project

1. Clone or download this repository.
2. Open the project folder.
3. Install the required libraries.
4. Launch Jupyter Notebook:

```bash
jupyter notebook
```

5. Open the `Handwritten_Digit_Recognition_CNN.ipynb` notebook.
6. Run the notebook cells sequentially.
7. Train the CNN model and view the evaluation results.
8. Upload a handwritten digit image using the notebook's upload interface to get a prediction.

## 📊 Model Training

The model is trained with the following configuration:

| Parameter | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Evaluation Metric | Accuracy |
| Epochs | 5 |
| Batch Size | 128 |
| Validation Split | 10% |
| Dropout Rate | 0.3 |

## 🔍 Prediction

The trained CNN model predicts the digit in an input image.

The image preprocessing steps include:

- Converting the image to grayscale.
- Adjusting image contrast.
- Applying thresholding.
- Cropping the digit.
- Resizing and centering the digit on a 28 × 28 canvas.
- Normalizing pixel values.

The model returns the predicted digit (0–9) and its highest Softmax probability as the confidence score.

## 💾 Model Saving

The trained model is saved in the following format:

```python
model.save("handwritten_digit_cnn.keras")
```

The saved model can be loaded later without training it again:

```python
from tensorflow.keras.models import load_model

model = load_model("handwritten_digit_cnn.keras")
```

## 🚀 Future Enhancements

- Improve prediction accuracy for different handwriting styles.
- Develop a web application using Flask or FastAPI.
- Add a drawing canvas for users to write digits directly.
- Extend the system to recognize handwritten alphabets.
- Deploy the application online.

## 👨‍💻 Project Team

Add your team members' names and roll numbers here.

## 📄 Conclusion

This project demonstrates how Convolutional Neural Networks can be used for handwritten digit recognition. By training a CNN model on the MNIST dataset, the system learns image features and classifies handwritten digits from 0 to 9.

The project provides practical experience with deep learning, image preprocessing, model training, evaluation, and image classification.
