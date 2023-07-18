# Vehicle-s-License-Plate-Detection
Automatic number-plate recognition is a technology that uses optical character recognition on images to read vehicle registration plates. This repository will illustrate how Azure Cognitive Services [https://azure.microsoft.com/en-us/products/ai-services#overview?activetab=pivot:azureopenaiservicetab] can be used to develop such a solution.

Custom Vision[https://learn.microsoft.com/en-us/azure/cognitive-services/Custom-Vision-Service/overview] will be used to develop object detection model will be used to identify the coordinates of a vehicle's number plate in an image. This will be used to crop the image to focus on the number plate. The Read API[https://learn.microsoft.com/en-us/azure/cognitive-services/computer-vision/overview-ocr] will than use this cropped image to perform optical character recognition (OCR) to extract the number plate from the image.


# Getting Started
# Setup the Environment
# Download Images
Sample images have been sourced from this[http://www.zemris.fer.hr/projects/LicensePlates/english/results.shtml] site from a database that contains over 500 images of the rear views of various vehicles (cars, trucks, busses), taken under various lighting conditions (sunny, cloudy, rainy, twilight, night light). This data will be used to train a custom vision object detection model and perform OCR.
# Develop Custom Vision Model
# Create Configuration File
# Run the Notebook



