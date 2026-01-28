---
title : "MindSight: Facial Emotion Recognition for Mental Health Monitoring"
date : 2025-06-24
image : "/img/posts/Screenshot 2026-01-21 133131.png"
description: "Artificial Intelligence, Machine Learning, Convolutional Neural Network (CNN), PyTorch, OpenCV"
---
### MindSight is a group project that is an advanced computer vision system designed to bridge the gap between human emotions and digital recognition. The project focuses on real-time detection and classification of facial expressions to provide deep insights into human emotional states for applications in mental health.


**Key Components of the Analysis**
- `Deep Learning Framework:` 
    - Utilized Convolutional Neural Networks (CNN) to perform robust feature extraction from facial landmarks.
- `Dataset:` 
    - Trained, tested, and validated on the FER-2013 dataset, which contains over 35,000 images categorized into seven basic emotional states such as angry, disgust, fear, happy, natural, sad, and surprise.
    {{< figure src="/img/posts/photo_2026-01-27_16-01-06.jpg"
    attr="Seven classes contained in FER-2013 dataset" >}}
- `Techniques:` 
    - EfficientNet-B0 backbone with Transformer attention
    - Data augmentation, affine transforms, focal loss, K-fold cross-validation
    - Integrated with Streamlit UI + real-time webcam + PHQ-9/GAD-7

**Results and Analysis**
- `High Precision Recognition:`
    - The data augmentation strategy produced the greatest macro average F1-score (0.6401) and equivalent performance (66.09% accuracy), indicating superior handling of the class imbalance. Furthermore, the data augmentation method demonstrated notable improvements in handling minority classes, especially for "disgust" (precision: 0.75) and "surprise" (recall: 0.80), demonstrating the usefulness of augmentation techniques in resolving class imbalance problems.
    {{< figure src="/img/posts/photo_2026-01-27_16-48-17.jpg"
    attr="Model performance comparison" >}}
- `Class Accuracy:`
    - Demonstrated strongest performance in detecting "Happy" (86.4%) and "Surprise" (74.2%) emotions.
- `Low Latency:`
    - Optimized the model to ensure an inference time of less than 30ms, allowing for seamless real-time interaction.
- `Feature Extraction:`
    - Successfully isolated subtle muscle movements in the eyebrow and mouth regions to distinguish complex emotions like "Fear" and "Sadness"

**GUI of Mindsight**
{{< figure src="/img/posts/photo_2026-01-27_16-54-47.jpg"
attr="A Web Application for Facial Emotion Recognition for Mental Health Assessment" >}}

{{< figure src="/img/posts/photo_2026-01-27_16-28-33.jpg"
attr="Live emotion detection using OpenCV camera" >}}

{{< figure src="/img/posts/photo_2026-01-27_16-55-05.jpg"
attr="Patient Health Questionnaire (PHQ-9) and General Anxiety Disorder (GAD-7) questionnaires" >}}

{{< figure src="/img/posts/photo_2026-01-27_16-55-19.jpg"
attr="Assessment result of the combined risk assessment between emotion analysis and questionnaire result" >}}