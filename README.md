# Cats vs Dogs Classification using CNN

## Problem Statement
The task is to classify images of cats and dogs using a Convolutional Neural Network (CNN). Given a dataset containing labeled images, the goal is to train a CNN model that can accurately predict whether a new image is of a **cat** or a **dog**.

## Objectives
- Prepare and preprocess the dataset for training and validation.  
- Apply data augmentation techniques to improve model generalization.  
- Build a CNN model using TensorFlow and Keras.  
- Train and evaluate the model on validation data.  
- Implement prediction functions for single and batch image classification.  
- Visualize training accuracy and validate performance.  

## Dataset
- **Source**: `Cats_Dogs.zip` dataset.  
- **Classes**:  
  - Cats 
  - Dogs 
- **Preprocessing**:  
  - Images resized to **150x150**.  
  - Data split into **80% training** and **20% validation**.  
  - Augmented with rotation, shift, shear, zoom, and horizontal flips.  

## Methodology
### 1. Data Preparation
- Extracted dataset and organized into `cats` and `dogs` folders.  
- Used `ImageDataGenerator` for preprocessing and augmentation.  

### 2. Model Building
- Built a **Sequential CNN** with:
  - Convolution + MaxPooling layers.  
  - Flatten and Dense hidden layers.  
  - Final **sigmoid** layer for binary classification.  

### 3. Training
- Optimizer: **SGD (lr=0.01)**  
- Loss: **Binary Crossentropy**  
- Epochs: **20**  

### 4. Evaluation
- Achieved **Validation Accuracy ~85-90%** (depending on dataset).  

### 5. Predictions
- Implemented custom prediction functions:  
  - `predict_image()` → predicts a single image.  
  - `predict_batch()` → predicts multiple images.  

### 6. Visualization
- Training vs Validation Accuracy plot.  
- Training vs Validation Loss plot.  

## Results
- Model successfully classified cats vs dogs with good accuracy.  
- Predictions on unseen images worked reliably.  
- Example Output:  
  ```python
  Prediction for images.webp: dog
  Prediction for download.jpg: cat

## Key Learnings

- Learned how to preprocess and augment image datasets.

- Built and trained a CNN from scratch using Keras.

- Understood overfitting risks and how validation monitoring helps.

- Gained experience in real-world classification and prediction systems.

## Conclusion

The CNN model effectively distinguished between cats and dogs, achieving strong validation accuracy. With further fine-tuning (e.g., more epochs, Adam optimizer, transfer learning), performance can be further improved.
