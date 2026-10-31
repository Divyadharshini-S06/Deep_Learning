# IMPLEMENTATION OF A SIMPLE AUTOENCODER FOR DIMENSIONALITY REDUCTION AND FEATURE LEARNING

## Description

This experiment implements a simple Autoencoder using the MNIST handwritten digit dataset for dimensionality reduction and feature learning. The input images are normalized and converted into one-dimensional vectors. An Autoencoder consisting of an Encoder, bottleneck layer, and Decoder is constructed and trained to compress the input data into a lower-dimensional representation and reconstruct the original images. The reconstruction performance is evaluated using Mean Squared Error (MSE), and the learned latent representations are visualized using Principal Component Analysis (PCA).

## Dataset

- **Dataset:** MNIST Handwritten Digit Dataset
- **Training samples:** 60,000
- **Testing samples:** 10,000
- **Image dimensions:** 28 × 28 pixels
- **Image type:** Grayscale
- **Original input features:** 784
- **Compressed features:** 32

## Data Preprocessing

- Loaded the MNIST handwritten digit dataset using TensorFlow/Keras.
- Explored the dataset and examined sample images.
- Converted pixel values into floating-point numbers.
- Normalized pixel values to the range 0 to 1.
- Reshaped 28 × 28 images into one-dimensional vectors of 784 features.
- Split the training data into training and validation datasets.
- Used the original input data as the target output for reconstruction.

## Autoencoder Model

- **Model:** Fully Connected (Dense) Autoencoder
- **Input dimension:** 784
- **Encoder layers:** 128 and 64 neurons
- **Bottleneck dimension:** 32
- **Decoder layers:** 64 and 128 neurons
- **Hidden layer activation:** ReLU
- **Output layer activation:** Sigmoid
- **Optimizer:** Adam
- **Loss function:** Mean Squared Error (MSE)

The Encoder compresses the original 784-dimensional input into a 32-dimensional latent representation. The Decoder reconstructs the original image using the compressed features.

## Model Training and Evaluation

- Trained the Autoencoder using the MNIST training dataset.
- Used 20 epochs and a batch size of 256.
- Monitored training and validation loss during training.
- Evaluated the trained model using the testing dataset.
- Calculated reconstruction Mean Squared Error (MSE).
- Generated a loss graph to analyze model performance.
- Compared original images with their reconstructed outputs.

The training and validation loss curves were used to observe how effectively the model learned to reconstruct the input images.

## Dimensionality Reduction and Feature Visualization

- Extracted latent-space representations using the trained Encoder.
- Reduced the original input dimensions from 784 to 32.
- Achieved a dimensionality compression ratio of 24.5:1.
- Applied Principal Component Analysis (PCA) to visualize the 32-dimensional latent representations in two dimensions.
- Used different colors to represent different handwritten digit classes.
- Reconstructed selected test images using the trained Decoder.
- Compared the original images with the decoded outputs.

## Observations

- The Autoencoder successfully learned compact representations of the MNIST images.
- The Encoder reduced the input dimensionality from 784 features to 32 features.
- The bottleneck layer retained important information required for image reconstruction.
- Training and validation loss decreased during model training.
- The Decoder reconstructed images that were visually similar to the original inputs.
- PCA visualization helped analyze the distribution of learned latent features.
- Reconstruction quality was evaluated using Mean Squared Error (MSE).

## Result

A simple Autoencoder was successfully implemented and trained using the MNIST handwritten digit dataset. The original 784-dimensional input data was compressed into a 32-dimensional latent representation and reconstructed using the Decoder. The reconstruction performance was evaluated using MSE, and the learned features were visualized using PCA.

## Conclusion

The experiment demonstrated the working and architecture of an Autoencoder for dimensionality reduction and feature learning. The Encoder compressed the input images into a lower-dimensional latent space, while the Decoder reconstructed the original images from the learned features. The experiment also demonstrated the importance of the bottleneck layer, reconstruction loss, and latent-space visualization in learning meaningful data representations.
