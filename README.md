# test-CV
# Downloading the YOLOV% into Google Colab
!git clone https://github.com/ultralytics/yolov5  # clone
## This command uses Git to clone the YOLOv5 repository from GitHub to your local environment, giving you access to YOLOv5 code and files.

%cd yolov5
## This command changes the working directory to yolov5, where all the cloned YOLOv5 files are now located

%pip install -qr requirements.txt comet_ml  # install
## installing the required libraries

import torch
import utils
display = utils.notebook_init()  # checks
## Are Python imports. torch is the main library for PyTorch, which YOLOv5 uses for model training and inference, and utils is a module within YOLOv5 containing utility functions.

# Connected to GDrive
from google.colab import drive
drive.mount('/content/drive')
## from google.colab import drive The line imports the drive module from google.colab, which allows the user to access Google Drive within Colab. drive.mount('/content/drive') This command mounts the Google Drive to a folder called /content/drive in the Colab file system. When the colab has been run, Google Colab will ask for permission to access the Drive.


# Installing datasets
!pip install datasets
## provides easy access to many popular datasets in machine learning, along with tools for data processing, caching, and loading.


# Installing Pyarrow
!pip install --upgrade pyarrow datasets
## pyarrow is a Python library for handling data in Apache Arrow format, which is optimized for high-performance data interchange. Apache Arrow is useful for efficient data processing and serialization, making it faster to load and save data, especially for large datasets.


# Importing load_dataset and TrashNet dataset
from datasets import load_dataset
## This imports the load_dataset function from the datasets library. load_dataset is a versatile function that allows you to load datasets directly from Hugging Face’s hub or from local files.
ds = load_dataset("garythung/trashnet")
## This line loads the TrashNet dataset, a dataset of images for waste classification, hosted under the Hugging Face user garythung.





