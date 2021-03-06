# Realtime Optical Character Recognition (OCR)
Optical Character Recognition (OCR) is the use of technology for converting of printed, scanned paper document, handwritten content, or image-only digital documents into a machine-readable and searchable digital data format. In essence, OCR involves identifying the included text and translating the characters into code that can be used for data processing. 

In this project OpenCV, Python, and Tesseract are used to implement Optical Character Recognition (OCR) for following tasks:

- **Text Detection** 
- **Text Recognition** 
- **Realtime Text Detection** 

Tesseract.v4 is utilized here which includes a highly accurate deep learning-based model for text recognition. The OpenCV OCR pipeline here includes two steps. The text detection is performed in the first step using OpenCV’s EAST text detector, a highly accurate deep learning algorithm trained to detect text in natural scene images. In the second step, the ROI (region of interest) of the detected texts will be passed to Tesseract to extract characters.  

## Sample Output

Following is a sample output of **Text Detection** function: 
![text_detection.png](images/text_detection.png)


Following is a sample output of **Text Recognition** function: 
![text_recognition.png](images/text_recognition.jpg)


Following is a sample output of **Realtime Text Detection** function: 
![video_output.gif](images/video_output.gif)


## Tesseract
Tesseract is a highly popular open source OCR engine, currently supported by Google. It needs to be installed, first. Please follow [this link](https://github.com/tesseract-ocr/tessdoc#binaries) for the instruction depending on the operating system:

![Tesseract_OCR_logo.png](images/Tesseract_OCR_logo.png)

##OpenCV’s EAST text detector
OpenCV’s EAST text detector is used here to detect the presence of text in an image. The output of EAST text detector is the bounding box (x, y)-coordinates of text ROIs. The extracted ROIs will be passed to Tesseract v4’s LSTM deep learning text recognition algorithm for the actual OCR results. Finally, the bounding boxes and OpenCV OCR results will also be drawn on output images.
The EAST text detector is pre-trained CNN network for text detection and ready to go. The model is already trained and readily provided with OpenCV. 

**Please download the file "frozen_east_text_detection.pb" and copy it in the root folder of the project.**


## Dependencies
* Pandas
* Numpy
* OpenCV
* Tesseract


How to use?
===========
The project is developed in Jupyter Notebooks which is automatically rendered by GitHub. The developed codes and functions for each step are explained in the notebook.












