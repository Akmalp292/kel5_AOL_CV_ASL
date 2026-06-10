
---
title: ASL Sign Language Detection
emoji: 🤟
colorFrom: green
colorTo: blue
sdk: docker
app_port: 5000
pinned: false
---

## Setup using Python virtual environment

First we create the virtual environment and clone the repository into it. 
Then, we install all dependencies before running the application.
```sh
python3 -m venv /path/to/venv
cd /path/to/venv
git clone https://github.com/user/name_project
source bin/activate
cd sign-language-detection
python3 -m pip install -r requirements.txt
python3 app.py
```

## Usage

- Click on 'Start' on the homepage to begin sign language detection on your video feed

- Permissions for video feed usage must be set to 'Allow'

- Write letters in American Sign Language to form words or phrases which show up on the console on the right

- Click on 'Play' button below the console to convert your sentences from text-to-speech for seamless communication

- For non-ASL users, you can refer to the English to ASL converter on the homepage 

- Follow 'Tips' under console for further instructions

## File Structure

```
.
├── app.py.............................Runs the Flask application and deploys all webpages
│                                      as well as calls necessary computational functions
├── datasets...........................Contains tar.gz file of the dataset and 
│                                      some necessary statistics for the dataset
├── LICENSE............................MIT LICENSE
├── models.............................TFLITE version models of MobileNet and EfficientNet
│   ├── model_efficientnet_v2s.tflite
│   └── model_mobilenet_v2.tflite
├── README.md
├── requirements.txt
├── screenshots........................Contains necessary visualizations about the 
│                                      model performance, data and website
├── static.............................Contains all js, css files and images used in the website
│   ├── connection.js
│   ├── opencv.js
│   └── style.css
├── templates..........................Contains all HTML templates deployed in the website
│   ├── about.html
│   ├── index.html.....................HTML template of the page where sign detection occurs
│   ├── landing.html
│   └── layout.html
├── train.py...........................Used to train the entire model, contains all 
│                                      ML techniques mentioned above
├── webcam_detect.py...................Loads the model and predicts the class from the 
│                                      frame input given as softmax probability which is sent 
│                                      back to the client's end
└── webcam.py..........................Used for testing ASL Sign Detection and preiction locally
```
