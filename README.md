# Vehicle-s-License-Plate-Detection
Automatic number-plate recognition is a technology that uses optical character recognition on images to read vehicle registration plates. This repository will illustrate how Azure Cognitive Services can be used to develop such a solution.

Custom Vision will be used to develop object detection model will be used to identify the coordinates of a vehicle's number plate in an image. This will be used to crop the image to focus on the number plate. The Read API will than use this cropped image to perform optical character recognition (OCR) to extract the number plate from the image.

Getting Started
Setup the Environment
Create a new conda environment from the environment.yml file:

conda env create -f environment/environment.yml
Note: you must have installed Anaconda.

Download Images
Sample images have been sourced from this site from a database that contains over 500 images of the rear views of various vehicles (cars, trucks, busses), taken under various lighting conditions (sunny, cloudy, rainy, twilight, night light). This data will be used to train a custom vision object detection model and perform OCR.

To download these images execute download_images.py in your conda environment:

conda activate opencv
python src/download_images.py
Note: this will create a directory called images.

Develop Custom Vision Model
To develop a custom vision model head over to Custom Vision and use a subset of the images that have been downlaoded in the prior step.

This can be done by:

Signing in and create a new project. Choose your own Name, Description and Resource (using your Azure subscription). Select Object Detection as the Project Type and leave the Domain as General.

Upload at least 15 images, select the number plate using the editor (give the number plate objects the same e.g. number-plate).

Train a model once all images have been loaded. Once training is complete a set of performance metrics will be displayed. The Quick Training option should be sufficient for this step.

Published the trained model as a REST API. Publishing generates the URL and authentication key for this service. This will be used in the next step.

Note: For more information follow the instructions in the Custom Vision Object Detector Quickstart guide.

Create Configuration File
Include the endpoints and access keys for the Custom Vision service and Computer Vision service in a file called cognitive-services.ini in a directory called configuration.

This file should be as follows:

[custom_vision]
key = <custom vision api key>
imgurl = <custom vision image file url>

[computer_vision]
key = <computer vision api key>
url = <computer vision url>
Run the Notebook
Open the jupyter notebook automatic-number-plate-recognition.ipynb, choose and image and run the notebook. Ensure you run this notebook in the conda environment you created earlier.
Train a model once all images have been loaded. Once training is complete a set of performance metrics will be displayed. The Quick Training option should be sufficient for this step.

Published the trained model as a REST API. Publishing generates the URL and authentication key for this service. This will be used in the next step.

Note: For more information follow the instructions in the Custom Vision Object Detector Quickstart guide.

Create Configuration File
Include the endpoints and access keys for the Custom Vision service and Computer Vision service in a file called cognitive-services.ini in a directory called configuration.

This file should be as follows:

[custom_vision]
key = <custom vision api key>
imgurl = <custom vision image file url>

[computer_vision]
key = <computer vision api key>
url = <computer vision url>
Run the Notebook
Open the jupyter notebook automatic-number-plate-recognition.ipynb, choose and image and run the notebook. Ensure you run this notebook in the conda environment you created earlier.
