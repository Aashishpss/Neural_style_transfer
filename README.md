# Neural Style Transfer

This project implements Neural Style Transfer (NST), which is a deep learning technique used to transfer the artistic style of one image (style image) onto another image (content image). By using a pre-trained VGG16 model, this method optimizes the content and style loss to generate an image that combines the content of one image with the style of another.
Requirements

To run this project, the following libraries are required:

    torch (for PyTorch)
    torchvision (for pre-trained models and transformations)
    PIL (for image handling)
    numpy (for numerical operations)
    matplotlib (for plotting and displaying images)

Install the required libraries using pip:

    pip install torch torchvision pillow numpy matplotlib

## Setup

Clone the repository or upload the notebook to your local Jupyter environment or Google Colab to run the code.

git clone https://github.com/yourusername/neural-style-transfer.git
cd neural-style-transfer

## Overview

The notebook follows these steps to perform Neural Style Transfer:

    Image Loading and Preprocessing:
        Content and style images are loaded and preprocessed using the torchvision.transforms library. The images are resized and normalized.

    Feature Extraction:
        A custom FeatureExtractor class extracts features from selected layers of a pre-trained VGG16 model, which is used to compute content and style loss.

    Loss Calculation:
        The content loss is computed by comparing the content of the generated image with the content image.
        The style loss is computed using the Gram matrix, which represents the style of an image by capturing correlations between different feature maps.

    Optimization:
        The generated image is initialized from the content image and optimized using the Adam optimizer.
        The optimization process minimizes both content and style loss, guided by their respective weights.

    Final Output:
        After optimization, the generated image is displayed with the style of the style image and the content of the content image.
