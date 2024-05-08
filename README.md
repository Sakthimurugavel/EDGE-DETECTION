# EX-06 EDGE-DETECTION

## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

## Step1:
Import all the necessary modules for the program.
## Step2:
Load a image using imread() from cv2 module.
## Step3:
Convert the image to grayscale
## Step4:
Using Sobel operator from cv2,detect the edges of the image.
## Step5:
Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

## Programs

Developed By:B.Venkata bharadwaj

Reg.No:212222240020


## Original Image
![OUT 1 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/0fa9fa94-51c7-4a7b-bb70-380bf99c9027)


### Convert image to grayscale and remove noise
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("fox.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```

### SOBEL EDGE DETECTOR

### SOBEL X AXIS :
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

### SOBEL Y AXIS :
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

### SOBEL XY AXIS :
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
### LAPLACIAN EDGE DETECTOR
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
### CANNY EDGE DETECTOR
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

SOBEL EDGE DETECTOR

Sobel X Axis Edge Detection

![out 2 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/541ed144-694c-4b75-aa90-dafca34cf863)


Sobel Y Sxis Edge Detection
![out 3 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/bcf2e2b4-2792-488b-8a15-2c2233b5b091)


Sobel XY Sxis Edge Detection

![out 4 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/4fd17969-c9ee-4f95-9684-b1f1e60305d6)


LAPLACIAN EDGE DETECTOR

![out 5 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/d132513b-410b-4722-a001-5fcb48e8c935)


CANNY EDGE DETECTOR

![out 6 6](https://github.com/Sakthimurugavel/EDGE-DETECTION/assets/118707246/0826cee8-8018-4325-a79d-4eb8c20fbf10)


## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
