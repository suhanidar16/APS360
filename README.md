# ElderSafe – AI-Powered Fall Detection & Human Posture Classification

Deep Learning | Computer Vision | PyTorch | ResNet18 | CNN | Vision Transformers

## Project Overview

ElderSafe is a deep learning-based computer vision system designed to identify human postures and detect potential falls, with the goal of improving safety monitoring for elderly individuals living independently.

I developed and evaluated multiple neural network architectures to classify human posture from indoor images, distinguishing between standing, sitting, lying, and fallen positions. The project explores how deep learning can be used for fall detection while accounting for challenges such as environmental variation, camera positioning, and model generalization.

## Key Features & Implementation

### 1. Computer Vision & Image Classification

- Developed an image classification pipeline to identify human postures and potential fall-related positions.
- Prepared and preprocessed image datasets for supervised learning, including image normalization and splitting the data into training, validation, and testing sets.
- Investigated how variations in camera perspectives, backgrounds, and lighting conditions affect classification performance.

### 2. Deep Learning Architecture Development

Implemented and compared several neural network architectures to determine which approaches were most effective for posture recognition:

- Artificial Neural Networks (ANNs): Explored fully connected networks as a baseline for image classification.
- Convolutional Neural Networks (CNNs): Developed models to learn spatial features and patterns associated with different human postures.
- Vision Transformers (ViTs): Experimented with attention-based image classification to evaluate their ability to recognize posture-related features.
- ResNet18 with Transfer Learning: Used a pretrained ResNet18 model and fine-tuned it for posture classification, achieving the strongest performance among the architectures tested.

### 3. Model Training & Optimization

- Developed model training and evaluation workflows using Python and PyTorch.
- Trained and tested different architectures using separate training, validation, and testing datasets.
- Monitored training and validation performance to identify overfitting and determine which models generalized most effectively.
- Examined misclassification patterns and classification thresholds to understand the tradeoff between missed falls and false detections.

### 4. Performance Evaluation & Generalization

- Achieved 99.46% classification accuracy on an internal held-out test dataset using a fine-tuned ResNet18 model.
- Evaluated model performance using accuracy, precision, recall, and confusion matrices.
- Conducted additional testing using independently staged images to assess how the model performed outside the original dataset.
- Identified potential dataset-source bias and sensitivity to camera angles, which revealed limitations that were not apparent from the internal test accuracy alone.

## Technical Stack

- Programming Language: Python
- Deep Learning Framework: PyTorch
- Architectures: ANN, CNN, Vision Transformer (ViT), ResNet18
- Techniques: Transfer Learning, Image Preprocessing, Supervised Learning, Model Fine-Tuning
- Evaluation: Accuracy, Precision, Recall, Confusion Matrices, Threshold Analysis

## Key Results

The optimized ResNet18 model achieved 99.46% accuracy on the internal held-out test dataset, making it the best-performing architecture evaluated in the project.

However, when I tested the model on independently staged images, I found that its performance was affected by differences in camera angles, backgrounds, and image composition. Although the model performed well on the original dataset, these additional tests showed that high test accuracy does not always translate to reliable performance in unfamiliar environments.

This was an important finding because fall detection requires more than simply recognizing patterns within a controlled dataset. A model intended for real-world use needs to handle different environments, body positions, and camera perspectives without producing excessive false detections or missing actual falls.

Through this project, I gained experience in deep learning architecture selection, transfer learning, training and evaluating computer vision models, and investigating how dataset characteristics influence model performance.

## Future Improvements

- Expand the training dataset with images from a wider range of indoor environments, lighting conditions, and camera perspectives.
- Investigate video-based models that use temporal information to distinguish accidental falls from intentional movements, such as lying down.
- Improve model robustness when people are partially obscured or positioned at unusual angles.
- Explore real-time inference and an automated alert system that could notify caregivers when a potential fall is detected.
