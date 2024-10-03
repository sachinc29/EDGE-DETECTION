# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.
a# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step 1:
Import all the necessary modules for the program.

### Step 2:
Load a image using imread() from cv2 module.

### Step 3:
Convert the image to grayscale

### Step 4:
Using Sobel operator from cv2,detect the edges of the image.

### Step 5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
```
Developed By: Sachin.C
Register No: 212222230125
```
```python
# Import necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('image.jpg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
```
### ORIGINAL IMAGE 

![image](https://github.com/user-attachments/assets/0145e0f1-a1f9-4443-90a1-6ada28b1d66d)

### SOBEL EDGE DETECTOR
```python
# Apply Sobel edge detector
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
```
![image](https://github.com/user-attachments/assets/6700fd14-d503-485e-bc27-5aede777b92f)

### LAPLACIAN EDGE DETECTOR
```python
# Apply Laplacian edge detector
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
```
![image](https://github.com/user-attachments/assets/18475ec2-7a0a-43ca-8287-272daecc8ee9)

### CANNY EDGE DETECTOR
```python
# Apply Canny edge detector
canny_edges = cv2.Canny(gray_image, 50, 150)
```
![image](https://github.com/user-attachments/assets/eb3725bf-dda1-4108-b32b-c5d30cf7d095)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
