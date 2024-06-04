# Vision Transformer for Driver Drowsiness Detection

This project involves using a Vision Transformer (ViT) model to detect driver drowsiness from EEG data. The dataset used is `1_postProcbest.mat`, which contains EEG recordings with 30 channels, 1250 timestamps, and 1609 samples.

## Project Steps

### 1. Data Loading

- Load the MATLAB file `1_postProcbest.mat` to extract the EEG data.
- The EEG data structure includes 30 channels, 1250 timestamps, and 1609 samples.

### 2. Data Preprocessing

- **Continuous Wavelet Transform (CWT)**:
  - Convert each channel's data into images using CWT.
  - Extract scaleograms from the EEG data, creating a dataset of images from the raw signal data.

### 3. Image Conversion

- Convert the extracted scaleograms into image format suitable for input into the Vision Transformer model.
- Each scaleogram is resized and normalized to create a consistent dataset of images.

### 4. Model Development

- **Vision Transformer (ViT)**:
  - Implement a custom ViT model.
  - Configure the model with the same parameters as the pretrained ViT model.
  - Adjust the model to handle the specific task of drowsiness detection from EEG data.

### 5. Model Training

- Train the Vision Transformer model using the processed image dataset.
- Use a suitable loss function and optimizer for the training process.
- Implement training and validation loops to monitor model performance.

### 6. Model Evaluation

- Evaluate the trained model on a test set to assess its performance.
- Calculate relevant metrics to measure the model's accuracy in detecting drowsiness.

## Conclusion

This project demonstrates the application of Vision Transformers for analyzing EEG data to detect driver drowsiness. By converting EEG signals into images, the powerful capabilities of ViT models can be leveraged to identify patterns associated with drowsiness.

## Getting Started

1. Clone the repository.
2. Ensure you have the required dependencies installed.
3. Follow the project steps outlined above to preprocess the data and train the model.

## References

- [scipy.io.loadmat](https://docs.scipy.org/doc/scipy/reference/generated/scipy.io.loadmat.html)
- [PyWavelets](https://pywavelets.readthedocs.io/)
- [Timm Vision Transformers](https://rwightman.github.io/pytorch-image-models/)
