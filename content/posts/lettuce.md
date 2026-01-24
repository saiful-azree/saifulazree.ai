---
title : 'Analysis of Monitoring the Growth and Health of Lettuce Using YOLOv9'
date : 2025-07-25
image: "/img/posts/Screenshot 2026-01-21 124915.png"
description: "Artificial Intelligence, Deep Learning, YOLO Algorithm, Roboflow, Google Colab, OpenCV"
---

##### The project utilizes the **YOLOv9 (You Only Look Once version 9)** algorithm to automate the monitoring of lettuce in a hydroponic system. This model was chosen for its superior accuracy and efficiency in real-time object detection compared to previous versions.


**Key Components of the Analysis**
- `Dataset and Classes:` 
    900 images are annotated with manual multi-class labels of growth stages (Week 1 to Week 4) and health (Healthy and Unhealthy) using Roboflow. 
    {{< figure src="/img/posts/Screenshot 2026-01-25 011746.png"
    attr="Box annotation process"  >}}  
- `Evaluation Metrics:` 
    - **Precision**: Measures the model's accuracy in identifying only relevant objects.
    - **Recall**: Indicates how well the model detecs all relevant objects.
    - **F1-score**: A single metric that balances both precision and recall to show how well the model performs overall.
    - **mAP@0.5**: Summarize the model's precision and recall performance across all classes at IoU threshold 0.5.
    - **mAP@0.5-0.95**: Averaged over multiple IoU thresholds (from 0.5 to 0.95). It gives more comprehensive evaluation of the model's localization perfomance.

**Results**
- `Model Version Comparison:`
    YOLOv9 achieved mAP@0.5 of 94% as well as mAP@0.5:0.95 of 83.6%, beating YOLOv8’s scores of mAP@0.5 and mAP@0.5:0.95 which is 84.4%, and 72.6% respectively. These results guarantee that YOLOv9 offers superior overall performance in both detection validity and generalization.
    {{< figure src="/img/posts/Screenshot 2026-01-25 020428.png"
    attr="Comparison on mAP performance between YOLOv9 and YOLOv8" >}}  
- `Model Inference (YOLOv9):`
    - **Dataset Images**: The model shows strong detection performance on images from the training and the test dataset. The model detects lettuce growth stage and health status with a high confidence score and correctly identifies the classes of “Week 2- Healthy” and “Week 3- Unhealthy” with accurately drawn bounding boxes. 
    {{< figure src="/img/posts/Screenshot 2026-01-25 023945.png"
    attr="Model inference on dataset images" >}}

    - **Unseen Images**: , the model continues to perform well on detecting and classifying the growth and health of the lettuces, such as "Week 2-Unhealthy" and "Week 3-Unhealthy," with reasonable levels of confidence. The model is clearly robust and has an ability to generalize far beyond the original dataset, which is necessary to fit real agricultural use cases.
    {{< figure src="/img/posts/Screenshot 2026-01-25 024020.png"
    attr="Model inference on unseen images" >}}


