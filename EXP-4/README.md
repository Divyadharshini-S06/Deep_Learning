# Transfer Learning Using Pre-trained Vision Models for Image Recognition

**Name:** Divyadharshini S  
**Roll No:** 24BAD022

## Overview

This experiment applies transfer learning using a pre-trained ResNet-50 model for image recognition and compares its performance with a Hugging Face Vision Transformer (ViT) model on real-world images.

## Software Used

- Python
- TensorFlow/Keras
- Google Colab
- Hugging Face Transformers
- KaggleHub
- Matplotlib
- GitHub

## Dataset

- **Dataset:** Intel Image Classification
- **Source:** Kaggle
- **Classes:** Buildings, Forest, Glacier, Mountain, Sea, Street

## Models Used

### Transfer Learning
- ResNet-50 (ImageNet Pre-trained)
- Frozen feature extraction layers
- Fine-tuned classification layers

### Hugging Face Model
- Vision Transformer (ViT)
- `google/vit-base-patch16-224`

## Evaluation Metrics

- Training Accuracy
- Validation Accuracy
- Testing Accuracy
- Training Loss
- Validation Loss

## Key Observations

- Transfer learning achieved faster convergence than training a CNN from scratch.
- ResNet-50 reused ImageNet features, improving learning efficiency.
- The Hugging Face ViT model successfully classified unseen images with meaningful predictions.

## Outcome

The experiment demonstrated that transfer learning significantly reduces training time while improving classification performance, making pre-trained models highly effective for image recognition tasks.
