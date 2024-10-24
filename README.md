# EXP NO-6
# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Program:
Developed by : Saileshkumar A

Register no:212222230126

### Convert image to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("dip6.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
### SOBEL EDGE DETECTOR
SOBEL X AXIS:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
SOBEL Y AXIS:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

```
SOBEL XY AXIS:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### LAPLACIAN EDGE DETECTOR:
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(lap)
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### CANNY EDGE DETECTOR:
```
canny=cv2.Canny(gray,120,150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny)
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
### SOBEL EDGE DETECTOR
### SOBEL X AXIS:

![image](https://github.com/premalatha-sureshbabu/EDGE-DETECTION/assets/120620842/214e4144-df2b-4921-8e02-057dc809aa06)

### SOBEL Y AXIS:

![image](https://github.com/premalatha-sureshbabu/EDGE-DETECTION/assets/120620842/7da387fb-5d3f-443c-b1aa-af55016b4868)

### SOBEL XY AXIS:

![image](https://github.com/premalatha-sureshbabu/EDGE-DETECTION/assets/120620842/4bcf554a-9b23-4661-9b69-aef676dc01ad)

### LAPLACIAN EDGE DETECTOR:

![image](https://github.com/premalatha-sureshbabu/EDGE-DETECTION/assets/120620842/ba27c183-daf4-431e-a84a-f45afdb5d371)

### CANNY EDGE DETECTOR

![image](https://github.com/premalatha-sureshbabu/EDGE-DETECTION/assets/120620842/f5654934-c494-40a1-bf48-b91cb0a4add3)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
