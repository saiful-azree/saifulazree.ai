---
title : Development of A Web-Based Trained Image Classification for Real-Time Object Recognition
date : 2024-06-22
image : "/img/posts/photo_2026-01-21_13-00-14.jpg"
description: "Artificial Intelligence, Machine Learning, STM32, Teachable Machine, STM32CubeAI, STM32CubeMX, STM32CubeIDE, ArduinoUNO"
---
#### This group project is about a work with Embedded AI (TinyML), integrating cloud-based training tools with hardware constraints. We designed and deployed a real-time image recognition system on a resource-constrained STM32H747I-DISCO microcontroller. The project aimed to bridge the gap between complex AI models and edge devices by enabling standalone image classification without reliance on continuous cloud processing.


**Key Components of the Analysis**
- `Hardware:` 
    - STM32H747I-DISCO board paired with a B-CAMS-OMV camera module.
- `Model Training:`
    - Utilized Google Teachable Machine to train a neural network on a custom dataset of development boards (Arduino UNO, ESP32 CAM, ESP8266, and STM32 Nucleo).
    {{< figure src="/img/posts/photo_2026-01-28_10-52-17.jpg"
    attr="Google Teachable Machine" >}}
- `Optimization:`
    - Employed STM32Cube.AI Developer Cloud to convert and optimize the TensorFlow Lite model into efficient C-code suitable for the microcontroller's architecture.
    {{< figure src="/img/posts/photo_2026-01-28_10-55-52.jpg"
    attr="User Interface of STM32Cube AI Developer Cloud" >}}
- `Deployment:`
    - Integrated the optimized model using STM32CubeIDE for firmware development and flashing.
    {{< figure src="/img/posts/photo_2026-01-28_11-00-45.jpg"
    attr="STM32CubeIDE" >}}

**Results and Analysis**
- `Classification Accuracy:` 
    - Achieved 100% detection accuracy for distinct classes like "Arduino" and "ESP32 CAM" under optimal lighting conditions.
    {{< figure src="/img/posts/photo_2026-01-28_11-15-13.jpg"
    attr="Confusion matrix" >}}
    {{< figure src="/img/posts/photo_2026-01-28_11-17-52.jpg"
    attr="Accuracy per epochs" >}}
- `Optimal Configuration:` 
    - Determined that a configuration of 250 Epochs, Batch Size 16, and a Learning Rate of 0.001 yielded the most stable results.
- `Performance Constraints:` 
    - The system operated at approximately 1.7 Frames Per Second (FPS) with an inference time of 590ms, highlighting the real-world trade-offs between model complexity and hardware processing power.
    {{< figure src="/img/posts/photo_2026-01-28_11-39-14.jpg"
    attr="The frame rate per second(fps) shows only 1.7 on the display" >}}
- `Hardware Challenges:` 
    - Identified critical limitations in the fixed-focus camera module, which required precise physical alignment for accurate inference, providing valuable insight for future hardware selection.

**Building Process**
{{< figure src="/img/posts/photo_2026-01-28_11-42-57.jpg"
    attr="Early development of the prototype" >}}
{{< figure src="/img/posts/photo_2026-01-28_11-43-00.jpg"
    attr="Finished product of the prototype" >}}
{{< figure src="/img/posts/photo_2026-01-28_11-43-04.jpg"
    attr="Output result of recognition for ESP 32 cam" >}}