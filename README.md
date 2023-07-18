# Vehicle-s-License-Plate-Detection
Automatic number-plate recognition is a technology that uses optical character recognition on images to read vehicle registration plates. This repository will illustrate how ([https://azure.microsoft.com/en-us/products/ai-services#overview?activetab=pivot:azureopenaiservicetab]) can be used to develop such a solution.

Custom Vision will be used to develop object detection model will be used to identify the coordinates of a vehicle's number plate in an image. This will be used to crop the image to focus on the number plate. The Read API will than use this cropped image to perform optical character recognition (OCR) to extract the number plate from the image.



