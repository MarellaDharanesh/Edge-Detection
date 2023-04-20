# Edge-Detection
## AIM:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## SOFTWARE REQUIRED:
Anaconda - Python 3.7

## ALGORITHM:
### Step 1:
Import the necessary modules.

### Step 2:
For performing edge detection on a image. 
- Sobel 
```python
sobelx=cv2.Sobel(gray,cv2.CV_64F,1,0,5)
sobely=cv2.Sobel(gray,cv2.CV_64F,0,1,5)
sobelxy=cv2.Sobel(gray,cv2.CV_64F,1,1,5)
```
- Laplacian
```python
lap=cv2.Laplacian(gray,cv2.CV_64F)
```
- Canny
```python
canny=cv2.Canny(gray,120,150)
```

### Step 3:
Display all the images with their respective edge detected images.

## PROGRAM:

```python
Developed by: Marella Dharanesh
RegisterNumber: 212222240062
```

``` Python
# Import the packages
import cv2
import matplotlib.pyplot as plt

# Load the image, Convert to grayscale and remove noise
img=cv2.imread("cap.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)

# SOBEL EDGE DETECTOR
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

# LAPLACIAN EDGE DETECTOR
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

# CANNY EDGE DETECTOR
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
## OUTPUT:
### SOBEL EDGE DETECTOR

![download](https://user-images.githubusercontent.com/118707669/233269518-b4b126fe-5a3a-44ac-a3f8-26c874f887bf.png)

![download](https://user-images.githubusercontent.com/118707669/233269668-f2b6f10b-44b9-47dd-8ba5-504445601650.png)




![download](https://user-images.githubusercontent.com/118707669/233269143-7f391b6a-44bc-46ec-b7d8-05bf1b047b14.png)


### LAPLACIAN EDGE DETECTOR

![download](https://user-images.githubusercontent.com/118707669/233269173-04aac574-c49a-4e74-88c6-c5c553e2e8a2.png)


### CANNY EDGE DETECTOR
![download](https://user-images.githubusercontent.com/118707669/233269195-9f0deffe-d719-474f-8a79-0c7e398ace23.png)


## RESULT:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
