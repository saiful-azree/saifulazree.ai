---
title : "Smart Dustbin for Arduino and IoT Learning Program with Melaka Technical School"
date : 2024-06-08
image : "/img/posts/photo_2026-01-21_13-00-15.jpg"
description: "IoT, Blynk, ArduinoIDE, C++, NodeMCU ESP8266, Sensors"
---
### Developed a smart waste management system integrating Internet of Things (IoT) technologies to automate trash collection and monitoring. The project served a dual purpose: solving environmental waste overflow issues and acting as a hands-on educational tool for students at Sekolah Menengah Teknik Melaka to learn Arduino and IoT fundamentals.


**Key Components of the Analysis**
- `Microcontroller Integration:`
    - Utilized the NodeMCU ESP8266 for its Wi-Fi capabilities, serving as the central processing unit to connect hardware with the cloud.
    {{< figure src="/img/posts/photo_2026-02-10_12-40-37.jpg"
    attr="Schematic diagram of the Smart Dustbin system" >}}
- `Sensor Fusion Strategy:`
    - **Lid Automation**: An external ultrasonic sensor detects human presence to trigger a Servo Motor, opening the lid automatically for hygienic, touch-free disposal.
    - **Fill-Level Monitoring**: An internal ultrasonic sensor continuously measures the distance to the trash. Data is processed to calculate the fill percentage.
- `IoT Platform:`
    - Integrated the Blynk Mobile App to display real-time status updates and send push notifications to the user when the bin reaches capacity.
    {{< figure src="/img/posts/photo_2026-02-10_15-09-23.jpg"
    attr="Blynk interface for displaying the status (currently offline)" >}}

**Results and Analysis**
- `System Performance:`
    - The system successfully demonstrated real-time logic, where the servo motor responded to proximity and the Blynk app accurately reflected fill levels.
- `Educational Impact:`
    - Pre and post program surveys indicated a significant increase in technical literacy. While initial knowledge of IoT was mixed, post-activity feedback showed that students successfully grasped how to connect components and use sensors.
    {{< figure src="/img/posts/photo_2026-02-10_15-27-40.jpg"
    attr="Explaining the connection between the sensors and the microcontroller" >}}
- `User Satisfaction:`
    - The program received a high satisfaction rating, validating the effectiveness of the "Service Learning" (SULAM) approach.
- `Sustainability Alignment:`
    - The project was analyzed against UN Sustainable Development Goals, specifically contributing to SDG 9 (Industry, Innovation, and Infrastructure) and SDG 11 (Sustainable Cities and Communities) by modernizing waste infrastructure.