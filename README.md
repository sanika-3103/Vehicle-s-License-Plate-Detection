# Vehicle's-License-Plate-Detection
Automatic number-plate recognition is a technology that uses optical character recognition on images to read vehicle registration plates. This repository will illustrate how Azure Cognitive Services [https://azure.microsoft.com/en-us/products/ai-services#overview?activetab=pivot:azureopenaiservicetab] can be used to develop such a solution.

Custom Vision[https://learn.microsoft.com/en-us/azure/cognitive-services/Custom-Vision-Service/overview] will be used to develop object detection model will be used to identify the coordinates of a vehicle's number plate in an image. This will be used to crop the image to focus on the number plate. The Read API[https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/overview-ocr] will than use this cropped image to perform optical character recognition (OCR) to extract the number plate from the image.

# SERVICES USED​

Storage account ​

Blob storage​

Custom Vision ​

LOGIC app​

SQL database ​

​
# Getting Started
# Setup the Environment
# Download Images
Sample images have been sourced from this[http://www.zemris.fer.hr/projects/LicensePlates/english/results.shtml] site from a database that contains over 500 images of the rear views of various vehicles (cars, trucks, busses), taken under various lighting conditions (sunny, cloudy, rainy, twilight, night light). This data will be used to train a custom vision object detection model and perform OCR.
# Develop Custom Vision Model
To develop a custom vision model head over to Custom vision and use a subset of the images that have been downloaded in the prior step This can be done by:​
​

1.Signing in and create a new project. Choose Name, Description and Resource (using your Azure subscription). Selecting Object Detection as the Project Type and leave the Domain as General.​

​

2.Upload at least 15 images, selecting the number plate using the editor (give the number plate objects the same e.g. number-plate).​

​

3.Train a model once all images have been loaded. Once training is complete a set of performance metrics will be displayed. The Quick Training option should be sufficient for this step.​

​

4.Published the trained model as a REST API. Publishing generates the URL and authentication key for this service. This will be used in the next step.​
# Upload and tag Images​
  
​ ![image](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/a5025d4b-005b-4f04-9e95-67aefbcae8d9)
# Train ​
![image](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/329fa6c6-e0bc-4139-a7a7-60f33f9351bc)
# Upload image​
![Screenshot (179)](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/c52f5d62-10ae-4d45-9c3c-e5cd23153fc8)
![1](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/01514196-354c-4c1f-9a12-4bce1f2673a6)

# Run the Trigger​
  ![Screenshot (11)](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/0cee0572-e5b1-4de2-81e4-fea1ab989950)
  ![2](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/b4ed5717-e70d-4d3b-85e8-a470ef0af2a2)
  ![3](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/c104acc1-19b5-468f-a3ce-b237840cb28d)


  # License plate successfully detected​
![Screenshot (12)](https://github.com/sanika-3103/Vehicle-s-License-Plate-Detection/assets/104089268/e813db34-aee5-4f97-bcd9-b06e29bf81db)







