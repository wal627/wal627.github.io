---
title: "Classifying Emotions Through Masks"
excerpt: "Using machine learning to determine emotions of faces in masks."
header:
  teaser: /assets/img/ML-1.png
gallery:
  - url: /assets/img/ML-1.png
    image_path: assets/img/ML-1.png
    alt: "placeholder image 1"
  - url: /assets/img/ML-2.png
    image_path: assets/img/ML-2.png
    alt: "placeholder image 2"
  - url: /assets/img/ML-3.png
    image_path: assets/img/ML-3.png
    alt: "placeholder image 3"
  - url: /assets/img/ML-4.png
    image_path: assets/img/ML-4.png
    alt: "placeholder image 4"
---

## Introduction

Emotion recognition involves developing machine learning models that can understand human emotions from various inputs like facial expressions, voice tones, body movements, and even text. The idea is to help machines interpret and respond to emotions in a human-like manner. This technology can be super useful in areas like customer service, healthcare, and even automotive safety by assessing a driver's emotional state.

For this project, I worked with a small group of engineers to develop our own models for emotion classification. However, our models contained a unique twist inspired by the COVID-19 pandemic. We wanted to see how well our models could classify emotions when people are wearing masks. We used the FER2013 dataset, which has thousands of images of human faces, to investigate this. Our big question was: Can models accurately classify emotions when the lower part of the face is covered by a mask? We hypothesized that they would struggle because masks hide many facial features that are crucial for understanding emotions.

## Literature Review

There have been significant advancements in emotion classification, especially with the use of deep learning models like Convolutional Neural Networks (CNNs). These models are great at automatically extracting features and are computationally efficient. For instance, the VGG model achieved a state-of-the-art accuracy of 73.28% on the FER2013 dataset by fine-tuning its parameters and using various optimization methods. Another study used an ensemble of up to eight CNN networks to achieve an accuracy of 75.23% on the same dataset.

When it comes to classifying emotions with masks, it's a different ball game. One study enhanced low-light images and analyzed upper facial features using CNNs, achieving 69.3% accuracy on the AffectNet dataset.

## Methods

We started with two main methods:

1. **SVM (Support Vector Machine)**
   - We used Scikit's SVC class for our SVM model. To handle the dataset's complexity, we used principal component analysis (PCA) to reduce dimensionality. Each 48x48 pixel image was broken down into an array of 2304 floats. We used 150 principal components, which captured about 90% of the variance. The model parameters were fine-tuned using cross-validation, and the trained model was tested on the dataset.

2. **MobileNetV2 CNN**
   - MobileNetV2 is a 53-layer deep CNN. We used TensorFlow Keras to load a pre-trained model (with weights from ImageNet) without the top classification layers. We added an output layer with 7 units using softmax activation. We also used data augmentation techniques like rotation and shifting to diversify our training data. The model was trained with the Adam optimizer and categorical cross-entropy loss.

## Results

Our results were pretty interesting:

- **SVM Model**: Achieved an accuracy of 42%, with the best performance on the “surprised” emotion (64%) and the worst on “fear” (31%). We knew SVMs might not perform well with noisy and overlapping data, but more principal components and features could improve accuracy.

- **MobileNetV2 Model**: Achieved around 60% accuracy. Training stopped after 20 epochs to prevent overfitting. The "surprise" emotion did best, while "happy" came in second, which was unexpected since we had the most data for "happy".

We also compared models trained on masked vs. unmasked data. Models trained on unmasked data performed better overall, but they struggled significantly (up to an 80% drop in accuracy) when tested on masked data. Models trained on masked data had a 20% drop when tested on unmasked data. Visualization techniques showed that unmasked-trained models focused on the eyes and mouth, while masked-trained models focused on facial contours.

## Conclusion and Future Steps

One big challenge was the imbalanced dataset, making it tough to develop models that worked well for minority classes. We used image augmentation and experimented with different loss functions to mitigate this. For future work, we might balance the dataset with more examples or try models trained on each emotion class independently and combine their predictions.

Check out our [project on GitHub](https://github.com/wal627/EmotionDetection) if you're interested!

## Gallery
{% include gallery caption="Emotion Detection Gallery" %}
