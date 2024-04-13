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
### Developed by : vasanth s
### reg no : 212222110052

### SOBEL EDGE DETECTOR
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("aizen.png",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

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
## Output:
![image](https://github.com/vasanth0908/EDGE-DETECTION/assets/122000018/43106b3f-5e30-45d3-9af8-cbdf7d70cf4c)

```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel y axis")
plt.axis("off")
plt.show()
```
## Output:

![image](https://github.com/vasanth0908/EDGE-DETECTION/assets/122000018/4bdb7cd8-6e3f-4253-9d1e-8e8ef9895217)

```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel xy axis")
plt.axis("off")
plt.show()
```
## Output:
![image](https://github.com/vasanth0908/EDGE-DETECTION/assets/122000018/20feb970-9543-435f-bf7c-a2e431b0b0ed)


### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(img,cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("laplacian")
plt.axis("off")
plt.show()

```

## Output:
![image](https://github.com/vasanth0908/EDGE-DETECTION/assets/122000018/0d8973e9-d673-4fd6-b8dd-4498b2d7761a)

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(img, 120, 150)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny_edges)
plt.title("canny_edges")
plt.axis("off")
plt.show()

```
## Output:
![image](https://github.com/vasanth0908/EDGE-DETECTION/assets/122000018/2e691e29-8ecb-435a-ab80-03107dde1457)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
