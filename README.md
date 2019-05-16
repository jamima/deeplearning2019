# Deep Learning 2019 Project
## Problem and Data Description
As our project, we chose the [iWildCam 2019 - FGVC6 Kaggle competition](https://www.kaggle.com/c/iwildcam-2019-fgvc6/overview). The problem focuses on identifying animal from Camera Traps (or Wild Cams). These cameras enable the collecting of large quantities of image data. This data has several possible uses, such as tracking the biodiversity and population density of the animals. Since the amount of data can be massive and the amount of "missfires" i.e. images that don't actually have animals in them is large, an automated recognition systems is highly useful.

The amount of data provided for the problem was massive for the tools we had available. The training set contains 196,157 images from 138 locations in South Carolina, and the test set contains 153,730 images from 100 locations in Idaho. in training data the majority of the image have the label "empty", meaning that there is no actual animal present in the image. Additionally, out of the 23 possible labels, only 14 were actually present in the training data.

## Our approach
We ended up using transfer learning with a DenseNet trained with ImageNet dataset. The majority of our work went into hadnling the image files in Google Drive in such a way that Google Colab could use them for the learning. We ended up splitting the data into several subfolders to avoid the timeout issues of the Google Drive when dealing with folders that have too many files. Similarly, due the enormousness of dataset we went forward with using only a part of it. Therefore, several adjustments were necessary to find the location of each image file and make the given dataframes hold information on the file location as well as the filename. With these adjustments, we modified code provided in [Pytorch kernel we found](https://www.kaggle.com/ateplyuk/iwildcam2019-pytorch-starter). Additionally, we found [the image processing kernel](https://www.kaggle.com/seriousran/image-pre-processing-for-wild-images) interesting to add on our approach as it showed promise in our experiments with it. We did not have enough time to change the given DenseNet transfer learning approach to utilize GAN networks as we originally planned. 

## Environment
* Language: Python
* Libraries: [PyTorch](https://pytorch.org/), [OpenCV](https://pypi.org/project/opencv-python/), [pandas](https://pandas.pydata.org/), [matplotlib](https://matplotlib.org/), [tqdm](https://tqdm.github.io/) 
* Development environment: [Google Colab](https://colab.research.google.com/notebooks/welcome.ipynb) and Google Drive

## Authors
* Jaakko Mattila ([jamima](https://github.com/jamima))
* Ilkka Saarnilehto ([ilnord](https://github.com/ilnord))

