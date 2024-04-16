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

## PROGRAM :
## Developed By : D.B.V. SAI GANESH
## Register Number : 212223240025
## Importing packages,load and convert to gray image
```
import cv2
import matplotlib.pyplot as plt
image=cv2.imread('flower.jpeg',0)
gray=cv2.cvtColor(image,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
plt.imshow(gray)
```
### Sobel Edge Detector
## Sobel X:
```
sobel_x = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobel_x,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
### Sobel Y
```
sobel_y = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobel_y,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
### Sobel XY
```
sobel_xy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobel_xy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
### Laplacian Edge Detector
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
### Canny Edge Detector
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:
## GRAY IMAGE:
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/1c589b76-c187-4142-9852-8558065c358d)

### SOBEL EDGE DETECTOR
### SOBEL X:
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/abc7fe68-097b-4363-8fb6-e216c8cfcf1b)

### SOBEL Y:
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/25a10a48-2a75-4abb-a99b-db819713432c)

### SOBEL XY:
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/db806390-dccf-4397-830f-e9b9e22a1170)

### LAPLACIAN EDGE DETECTOR
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/3159aebd-634d-4894-b1c4-7d53127e706c)


### CANNY EDGE DETECTOR
![image](https://github.com/saiganesh2006/EDGE-DETECTION/assets/145742342/8ec3e8b0-4f49-4da1-ac25-3790c8328b50)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
