### Deploying ML Model with the use REST API
##### ML Model for Object Detection using TensorFlow2, OnenCV, cvlib

Technologies:
- Python 3;
- TensorFlow 2;
- OpenCV;
- cvlib;
- FastAPI.

To explore the simple toy dataset (images-meetings.zip) and Object Detection algorithm:
- run ObjectDetection.ipynb.

To run the code locally (for testing purposes):
- cd to Project directory
- python3 -m venv venv
- source venv/bin/activate
- pip install -r server/requirements.txt
- cd ./server
- python3 server.py

To perform a deploy (for example on heroku.com):
- cd ./server
- create Docker image:
   - docker build -t ob-det-model .
- deploy.

For Object Detection is used cvlib that is a very simple but powerful library for object detection that is fueled by OpenCV and Tensorflow.
For server-client interactions using REST API we apply FastAPI.
FastAPI has a built-in client for the interaction with a server (localhost:8000/docs).
To test the server using built-in FastAPI's client:
- enter on it, click on the "Try it out" button
- You can choose a model from the model field (if you select the full YOLO model
the server will be stuck until the weights for this model are downloaded)
and a file which should be the image in which you want the server to detect objects
- Submit an image from your local filesystem by clicking the "Choose File" button,
then click on the blue "Execute" button to send an HTTP request to the server
- After doing so, scroll down and you will see the response from it


#### License

This project is licensed under the terms of the MIT license.