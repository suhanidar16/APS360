**ElderSafe – AI-Powered Fall Detection & Human Posture Classification
**
**Deep Learning | Computer Vision | PyTorch | ResNet18 | CNN | Vision Transformers**

## Project Overview

ElderSafe is a deep-learning-powered computer vision system designed to identify human postures and detect potential falls, with the goal of improving safety monitoring for elderly individuals living independently.
I developed and evaluated multiple neural network architectures to classify human posture from indoor images, distinguishing between standing, sitting, lying, and fallen positions. The project explores how artificial intelligence can support early detection of potentially dangerous situations while addressing challenges such as environmental variation, camera positioning, and model generalization.

## Key Features & Implementation

### 1. Computer Vision & Image Classification
- Developed an image-based classification pipeline to identify human postures and potentially dangerous fall-related positions.
- Prepared and preprocessed image datasets for supervised deep learning, including image normalization and data partitioning for training, validation, and testing.
- Investigated how environmental characteristics and camera perspectives influence classification reliability.

### 2. Deep Learning Architecture Development
Implemented and compared multiple neural network architectures to evaluate their suitability for posture recognition:

- **Artificial Neural Networks (ANNs):** Explored fully connected architectures as a baseline for image classification.
- **Convolutional Neural Networks (CNNs):** Developed models capable of learning spatial features and posture-related visual patterns.
- **Vision Transformers (ViTs):** Experimented with attention-based image classification to capture relationships between image regions.
- **ResNet18 with Transfer Learning:** Leveraged pretrained convolutional representations and fine-tuning to improve classification performance.

### 3. Model Training & Optimization
- Built deep learning workflows using Python and PyTorch.
- Trained and evaluated architectures using separate training, validation, and test datasets.
- Analyzed training behavior, overfitting, and misclassification patterns to guide model improvements.
- Explored classification threshold adjustments to better understand the tradeoff between missed detections and false alerts.

### 4. Performance Evaluation & Generalization
- Achieved **99.46% classification accuracy on an internal held-out test dataset** using an optimized ResNet18 transfer-learning model.
- Evaluated model performance using precision, recall, and confusion matrices.
- Conducted additional testing using staged real-world images to investigate model generalization beyond the original dataset.
- Identified potential dataset-source bias and camera-angle sensitivity, highlighting limitations of relying exclusively on benchmark accuracy.

## Technical Stack
- **Programming Language:** Python
- **Deep Learning Framework:** PyTorch
- **Architectures:** ANN, CNN, Vision Transformer (ViT), ResNet18
- **Techniques:** Transfer Learning, Image Preprocessing, Supervised Learning, Model Fine-Tuning
- **Evaluation:** Accuracy, Precision, Recall, Confusion Matrix, Threshold Analysis

## Key Results
The optimized ResNet18 model achieved 99.46% accuracy on the project's internal test dataset, demonstrating the effectiveness of transfer learning for posture-based classification.
However, testing with independently staged images revealed important generalization challenges. Differences in camera angles, backgrounds, and dataset sources influenced model reliability, emphasizing the importance of evaluating AI systems beyond controlled test conditions.
This project strengthened my understanding of deep learning architecture selection, computer vision pipelines, transfer learning, model evaluation, and the challenges of developing reliable AI systems for safety-critical applications.

## Future Improvements
- Expand the dataset with more diverse environments, camera perspectives, and lighting conditions.
- Investigate temporal video analysis to distinguish accidental falls from intentional lying-down movements.
- Improve robustness against occlusions, unusual body positions, and background variation.
- Explore real-time inference and alert-generation capabilities for future monitoring applications.
