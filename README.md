# Overview
This project explores the application of Generative Adversarial Networks (GANs) to generate synthetic images for various datasets, including:

MNIST: Handwritten digits
CelebA: Human faces
CIFAR-10: Diverse object categories
We implemented and tested different GAN architectures, utilizing advanced techniques such as batch normalization, LeakyReLU activations, and transpose convolution layers. This project aims to push the boundaries of image generation by experimenting with GAN models to produce realistic, high-fidelity images.

The findings of this project have important implications for industries such as healthcare, entertainment, and security, where GANs can generate synthetic datasets or aid in enhancing image quality.

# Key Features
Handwritten Number Generation:

Dataset: MNIST (28x28 grayscale images)
Architecture: Upsampling layers with batch normalization and LeakyReLU activations in the generator, fully connected layers with dropout in the discriminator.
Evaluation Metrics: Fréchet Inception Distance (FID), Inception Score (IS).
Human Face Generation:

Dataset: CelebA (200,000 celebrity images)
Architecture: Transpose convolution layers for upsampling in the generator; convolutional layers with LeakyReLU and dropout in the discriminator.
Evaluation Metrics: Inception Score (IS), FID.
CIFAR-10 Image Generation:

Dataset: CIFAR-10 (60,000 32x32 color images across 10 categories)
Architecture: Transpose convolution layers in the generator and convolutional layers in the discriminator.
Evaluation Metrics: Inception Score (IS), FID.
Project Structure
The project is structured as follows:

## Data Preparation:
Each dataset required custom preprocessing steps due to their varying complexities (MNIST, CelebA, CIFAR-10).
Model Architectures:
Unique GAN architectures for each dataset, with key components like transpose convolution, batch normalization, and LeakyReLU activations.
## Training Process:
Generator and discriminator trained using adversarial loss functions.
Optimization techniques include stochastic gradient descent and gradient penalty.
## Evaluation:
Models evaluated on qualitative (visual inspection) and quantitative (IS and FID) metrics to assess the quality and diversity of the generated images.
## Results
MNIST: The GAN model produced highly realistic handwritten digits, with high scores on both IS and FID metrics.
CelebA: Generated faces were generally realistic, though some artifacts indicated the need for further refinement.
CIFAR-10: While some categories were well-represented, improvements are needed in certain object categories.
## Methodology
The methodology for each dataset involved the following steps:

Data Preparation: Processing datasets according to the needs of the GAN model.
Generator Network: Designed to progressively upscale the input noise into high-resolution images.
Discriminator Network: Trained to distinguish between real and fake images using convolutional layers and LeakyReLU activations.
Loss Functions and Optimization: The generator minimizes the discriminator's ability to differentiate between real and fake images, using loss functions like binary cross-entropy.
