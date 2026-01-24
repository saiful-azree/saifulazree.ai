---
title : 'Analysis of Monitoring the Growth and Health of Lettuce Using YOLOv9'
date : 2025-07-25
image: "/img/posts/Screenshot 2026-01-21 124915.png"
description: "Artificial Intelligence, Deep Learning, YOLO Algorithm, Roboflow, Google Colab, OpenCV"
---

### The project utilizes the **YOLOv9 (You Only Look Once version 9)** algorithm to automate the monitoring of lettuce in a hydroponic system. This model was chosen for its superior accuracy and efficiency in real-time object detection compared to previous versions.

**Key Components of the Analysis**
- `Dataset and Classes:` 
    900 images are annotated with manual multi-class labels of growth stages (Week 1 to Week 4) and health (Healthy and Unhealthy) using Roboflow. 
    {{< figure src="/img/posts/Screenshot 2026-01-25 011746.png"
    alt="Box annotation process" 
    attr="Box annotation process" 
    attrlink="" >}}  
- `Evaluation Metrics:` 
    - **Precision:**Measures the model's accuracy in identifying only relevant objects.
    - **Recall:**Indicates how well the model detecs all relevant objects.
    - **F1-score:**A single metric that balances both precision and recall to show how well the model performs overall.
    - **mAP@0.5:**Summarize the model's precision and recall performance across all classes at IoU threshold 0.5.
    - **mAP@0.5-0.95:**Averaged over multiple IoU thresholds (from 0.5 to 0.95). It gives more comprehensive evaluation of the model's localization perfomance.

**Results**
- `Model Version Comparison:`
    YOLOv9 achieved mAP@0.5 of 94% as well as mAP@0.5:0.95 of 83.6%, beating YOLOv8’s scores of mAP@0.5 and mAP@0.5:0.95 which is 84.4%, and 72.6% respectively. These results guarantee that YOLOv9 offers superior overall performance in both detection validity and generalization. Therefore, YOLOv9 is an excellent model for this application in monitoring lettuce, despite its slightly lower precision. The performance is mainly improved by the more advanced architecture of YOLOv9, such as the GELAN backbone, which results in more effective feature extraction.
    {{< figure src="/img/posts/Screenshot 2026-01-25 020428.png"
    alt="Box annotation process" 
    attr="Box annotation process" 
    attrlink="" >}}  


