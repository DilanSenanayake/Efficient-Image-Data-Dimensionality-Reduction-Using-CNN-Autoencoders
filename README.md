# Efficient-Image-Data-Dimensionality-Reduction-Using-CNN-Autoencoders
This project features a Convolutional Neural Network (CNN) Autoencoder focused on dimensionality reduction for image data. The model compresses images into lower-dimensional representations while preserving essential features, making it ideal for tasks such as feature extraction and noise reduction. 

## Dataset
- **Location:** Provide the path to your dataset in the `dataset_dir` variable.
- **Structure:** The dataset should be organized in a directory structure suitable for `ImageDataGenerator`, with subdirectories representing different classes.
- **url:** https://www.kaggle.com/datasets/vuppalaadithyasairam/bone-fracture-detection-using-xrays/data

## Model Architecture
The autoencoder consists of two parts:
- **Encoder:** Compresses the input image into a lower-dimensional representation.
- **Decoder:** Reconstructs the image from the compressed representation.

The model is built using TensorFlow and Keras, with the following layers:
- **Encoder:**
  - Convolutional layers with ReLU activation and strides of 2 for downsampling.
  - Feature extraction with increasing filter sizes.
  
- **Decoder:**
  - Transposed convolutional layers for upsampling.
  - Final layer uses sigmoid activation to output pixel values in [0, 1].

## Training
The model is trained using the Mean Squared Error (MSE) loss and the Adam optimizer. The dataset is split into training and testing sets with an 80-20 ratio.