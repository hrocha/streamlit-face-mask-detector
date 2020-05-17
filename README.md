# streamlit-face-mask-detector
A simple [Streamlit](https://www.streamlit.io/) frontend for face mask detection in images using a pre-trained [Keras](https://keras.io/) CNN model + [OpenCV](https://opencv.org/) and model interpretability.  
## General info
This example has been implemented as part of my evaluation of the Streamlit framework. It uses OpenCV to detect faces in the input images and a CNN as mask/no-mask binary classifier applied to the face ROI. The Deep Learning model currently used has the architecture suggested by Adrian Rosebrock [here](https://www.pyimagesearch.com/2020/05/04/covid-19-face-mask-detector-with-opencv-keras-tensorflow-and-deep-learning/) and has been trained using [this](https://github.com/prajnasb/observations/tree/master/experiements/data) image data set. The trained model has been shared in this repo. The face detector algorithm can be downloaded from [here](https://github.com/Shiva486/facial_recognition): the Caffe model and its descriptor need then to be saved into the *face_detector* directory.    
## Deep Learning Explanation
Once an image has been uploaded, the classification happens automatically. It is then possible to apply some interpretability methods for neural network understanding. The UI presents two buttons to apply the following methods:
- Grad CAM: it visualizes how parts of the input image affect a CNN output by looking into the activation maps.
- Occlusion Sensitivity: it visualizes how parts of the input image affect a CNN confidence by iteratively occluding parts.
## Usage
After cloning this repository and have downloaded the face detector algorithm, you need to create a virtual environment and install the application dependencies  
```pip install -r requirements.txt```
Then you can execute the application through the streamlit command  
```streamlit run streamlit_face_mask_detector.py```

