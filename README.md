# Dlib-vs-OpenCV
Compares face recognition performance of [dlib](http://dlib.net/) and [OpenCV](http://opencv.org/) using the [WIDER face detection benchmark](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/).

### Prerequisites
Python 3, OpenCV and dlib.

### Installation
Download the WIDER FACE cross validation set from [here](https://drive.google.com/open?id=0B9o_M4g2M0GxX05pWENkeHdDWkE) and place it into the `data` directory. To use the training or test sets (although it should not matter), download the appropriate images and labels from [here](http://mmlab.ie.cuhk.edu.hk/projects/WIDERFace/) then run the `PreprocessLabels.ipynb` notebook to transform the MATLAB given labels into a Python dictionary (more details below).

### Running
Just run `DetectedFacesOpenCV-Dlib.ipynb` as a Jupyter notebook.

### More Details
Images and labels should be placed in the `data` directory. Images have not been uploaded but you can download them [here](https://drive.google.com/open?id=0B9o_M4g2M0GxX05pWENkeHdDWkE). Labels describe properties of images, such as the location of faces, whether they are occluded, blurred, or poorly illuminated.

The WIDER FACE benchmark provides image labels as MATLAB matrices. `PreprocessLabels.ipynb` loads the MATLAB matrix labels and rewrites them as a Python dictionary, saving the result as a Python pickle into the `data` folder.

`DetectedFacesOpenCV-Dlib.ipynb` uses the `data/labels.ipynb` labels and `data/WIDER/*/*.jpg` images for analysis.

`Dlib.ipynb` and `OpenCV.ipynb` are simple attempts at using Dlib and OpenCV for face detection in a single image.

### Authors
See the list of contributors [here](https://github.com/andreimuntean/dlib-vs-opencv/graphs/contributors).