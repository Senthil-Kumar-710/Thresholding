# Thresholding of Images
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Load the necessary packages.
<br>

### Step2:
Read the Image and convert to grayscale.
<br>

### Step3:
Use Global thresholding to segment the image.
<br>

### Step4:
Use Adaptive thresholding to segment the image.
<br>

### Step5:
Use Otsu's method to segment the image.
<br>

### Step 6:
Display the results.
<br>
## Program

## Developed By: Senthil Kumar S
## Reg No: 21221230091

<br>

### Load the necessary packages
```python
import cv2
import numpy as np
import matplotlib.pyplot as plt
```

### Read the Image and convert to grayscale
```python
ori_img=cv2.imread('roy.jpg')
ori_img=cv2.resize(ori_img,(460,250))
gray_img=cv2.cvtColor(ori_img,cv2.COLOR_BGR2GRAY)
```
<br>

### Use Global thresholding to segment the image
```python
ret,thresh_img1=cv2.threshold(gray_img,86,255,cv2.THRESH_BINARY)
ret,thresh_img2=cv2.threshold(gray_img,86,255,cv2.THRESH_BINARY_INV)
ret,thresh_img3=cv2.threshold(gray_img,86,255,cv2.THRESH_TOZERO)
ret,thresh_img4=cv2.threshold(gray_img,86,255,cv2.THRESH_TOZERO_INV)
ret,thresh_img5=cv2.threshold(gray_img,100,255,cv2.THRESH_TRUNC)
```
<br>

### Use Adaptive thresholding to segment the image
```python
thresh_img6=cv2.adaptiveThreshold(gray_img,255,cv2.ADAPTIVE_THRESH_MEAN_C,cv2.THRESH_BINARY,11,2)
thresh_img7=cv2.adaptiveThreshold(gray_img,255,cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY,11,2)
```
<br>

### Use Otsu's method to segment the image 
```python
ret,thresh_img8=cv2.threshold(gray_img,0,255,cv2.THRESH_BINARY+cv2.THRESH_OTSU)
```
<br>

### Display the images
```python
cv2.imshow('original',ori_img)
cv2.imshow('gray',gray_img)
cv2.imshow('binary threshold',thresh_img1)
cv2.imshow('binary to inverse threshold',thresh_img2)
cv2.imshow('to zero threshold',thresh_img3)
cv2.imshow('to zero to inverse threshold',thresh_img4)
cv2.imshow('truncate threshold',thresh_img5)
cv2.imshow('mean adaptive threshold',thresh_img6)
cv2.imshow('gaussian adaptive threshold',thresh_img7)
cv2.imshow('otsu thresold',thresh_img8)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

<br>

## Output

## Original Image and Gray Image

### Original
![original](https://user-images.githubusercontent.com/93860256/235345751-4825c1be-7c32-4f15-a635-fb0d505c138c.png)
<br>

### Gray
![gray](https://user-images.githubusercontent.com/93860256/235345752-80f810c3-6136-4f93-a8b8-a6a460524b30.png)
<br>

## Global Thresholding

### Binary Threshold
![binary threshold](https://user-images.githubusercontent.com/93860256/235345846-c26d0424-e860-4939-96bf-2a47d5911190.png)
<br>
### Binary to Inverse Threshold
![binary to inverse threshold](https://user-images.githubusercontent.com/93860256/235345848-b2c44608-e5b3-452f-8096-c7474cf6dae5.png)
<br>
### To Zero Threshold
![to zero threshold](https://user-images.githubusercontent.com/93860256/235345850-51f76d04-efd0-41a7-8783-45fb674e15a1.png)
<br>
### To Zero to Inverse Threshold
![to zero to inverse threshold](https://user-images.githubusercontent.com/93860256/235345852-45ce6d13-e2b9-4224-9f0c-591f4c896657.png)
<br>
### Truncate Threshold
![truncate threshold](https://user-images.githubusercontent.com/93860256/235345855-68d1d986-e2fe-4e84-9d3f-df80b182e03e.png)
<br>

## Adaptive Thresholding

### Mean Adaptive Threshold
![mean adaptive threshold](https://user-images.githubusercontent.com/93860256/235345687-8d5724c5-3ff8-4631-8ac0-9f0c54f21b63.png)
<br>

### Gassian Adaptive Threshold
![gaussian adaptive threshold](https://user-images.githubusercontent.com/93860256/235345703-72b046f8-3925-45c2-b794-66267321c78e.png)
<br>


## Optimum Global Thesholding using Otsu's Method
![otsu thresold](https://user-images.githubusercontent.com/93860256/235345667-fecc52ea-06f0-4bca-88c9-534117ed6e7f.png)
<br>
<br>

## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.

