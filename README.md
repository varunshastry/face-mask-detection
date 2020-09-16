# face-mask-detection

What?
Identify if a person in front of a webcam is wearing a face mask.

How?
Employ supervised learning. Using python libraries and Jupyter notebook, models would be trained on a data set of images that contain people wearing face masks and people not wearing face masks. The trained model(s) would then be verified using webcam, and of course a face mask.

Takeaways:
Basics of Python
Basics of Jupyter notebook
Basics of Machine Learning

Tools/Libraries:
Jupyter-notebook 6.1.3
Python (and pip) 3.8
Python libraries
keras
matplotlib
numpy
opencv-python
scikit-learn
scipy
tensorflow

Setup:
Download and install python (and pip) 3.8 - https://www.python.org/downloads/
Set the env variable "PYTHONPATH". For example → export PYTHONPATH=/usr/local/lib/python3.8/site-packages
Install pip →python -m pip install --upgrade pip setuptools wheel  (// run it from command prompt)
Install the libraries using → pip3.8 install -U keras matplotlib numpy opencv-python scikit-learn scipy tensorflow
Download and install Jupyter Notebook - https://jupyter.org/install

How to run:
Download the image data set from here into a directory (say /tmp/face-mask-detection/dataset)
Unzip the downloaded dataset into 2 directories - train and test
Download the source code (train.py and test.py) into a directory (say /tmp/face-mask-detection)
In the train.py file, set the following variables to corresponding values:
TRAINING_DIR = "/tmp/face-mask-detection/dataset/train"
VALIDATION_DIR = "/tmp/face-mask-detection/dataset/test"
Run the train.py:
cd ~/face-mask-detection
python3.8 train.py
Successful execution of above command would result in the generation of models in the /tmp/face-mask-detection directory (like model2-001.model, model2-002.model, etc)
In the test.py file, make the following modifications:
classifier = cv2.CascadeClassifier('<absolute-path-to-haarcascade_frontalface_default.xml>')
Run the test.py by passing the generated model names as parameters to the script:
python3.8 test.py model2-001.model model2-002.model

Resources:
Image data set → https://data-flair.s3.ap-south-1.amazonaws.com/Data-Science-Data/face-mask-dataset.zip
Python basics → https://www.w3schools.com/python/default.asp
Using Jupyter Notebook → https://www.dataquest.io/blog/jupyter-notebook-tutorial/
Machine learning basics:
https://machinelearningmastery.com/basic-concepts-in-machine-learning/
https://towardsdatascience.com/machine-learning-basics-part-1-a36d38c7916
