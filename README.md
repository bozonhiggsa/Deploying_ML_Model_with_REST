### Deploying ML Model with the use REST API
##### ML Model for Object Detection using TensorFlow2, OnenCV, cvlib

Imlementation is based on the original work for artistic style transfer with neural networks proposed a slow optimization algorithm that works on any arbitrary painting.

Technologies:
- Python 3;
- TensorFlow 2;
- OpenCV;
- cvlib;
- FastAPI.

To explore the simple toy dataset (images-meetings.zip) and Object Detection algorithm:
- run ObjectDetection.ipynb.

To perform a deploy (for example on heroku.com):
- cd ./server
- create Docker image:
   - docker build -t ob-det-model .
- deploy.

For Object Detection is used cvlib that is a very simple but powerful library for object detection that is fueled by OpenCV and Tensorflow.
For server-client interractions using REST API we apply FastAPI.

#### License

This project is licensed under the terms of the MIT license.