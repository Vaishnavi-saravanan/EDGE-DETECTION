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

# PROGRAM:
```
DEVELOPED BY: VAISHNAVI S
REGISTER NUMBER: 212222230165
```
# IMPORT PACKAGES AND LOAD IMAGES
```
import cv2
import matplotlib.pyplot as plt

img=cv2.imread("edge.jpg",0)
gray=cv2.cvtColor(img,cv2.COLOR_GRAY2RGB)
gray = cv2.GaussianBlur(gray,(3,3),0)
```
# SOBEL EDGE DETECTOR:
SOBEL X:
```
sobelx = cv2.Sobel(gray,cv2.CV_64F,1,0,ksize=5)
plt.imshow(sobelx,cmap='gray')
plt.title("Sobel X axis")
plt.axis("off")
plt.show()
```
SOBEL Y:
```
sobely = cv2.Sobel(gray,cv2.CV_64F,0,1,ksize=5)
plt.imshow(sobely,cmap='gray')
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()
```
SOBEL XY:
```
sobelxy = cv2.Sobel(gray,cv2.CV_64F,1,1,ksize=5)
plt.imshow(sobelxy,cmap='gray')
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()
```
# LAPLACIAN EDGE DETECTOR:
```
lap=cv2.Laplacian(gray,cv2.CV_64F)
plt.imshow(lap,cmap='gray')
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()
```
# CANNY EDGE DETECTOR:
```
canny=cv2.Canny(gray,120,150)
plt.imshow(canny,cmap='gray')
plt.title("Canny Edge Detector")
plt.axis("off")
plt.show()
```
## Output:

# ORIGINAL IMAGE
![318408481-918b52c9-7b38-49ec-83a8-ce40b9a0495d](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/1a2c890d-2baf-42c2-9d65-15be30b9372d)
### SOBEL EDGE DETECTOR
![318408539-9b9cddf5-2c94-44fe-927a-5d3e3eeee552](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/e2e2ba4e-98aa-4100-80d4-d2be4d54e05a)
![318408550-e5b0318a-c102-4f90-a76d-4f61b9321035](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/f1003234-cb8a-42b2-98bf-f4c7f8d06589)
![318408565-bc5ede85-aabf-4b7f-8b2f-191d78911b9e](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/cb34e606-5706-4025-9769-06831eda4b44)

### LAPLACIAN EDGE DETECTOR
![318408666-1e91aada-fe49-4789-8d4e-1f02e2fc0965](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/ffffb83b-9514-448a-82e7-8ff55fa08ca9)


### CANNY EDGE DETECTOR
![318408677-c0df0b60-34b9-45bb-aec3-0a6e9380499b](https://github.com/Vaishnavi-saravanan/EDGE-DETECTION/assets/118541897/24221a91-151a-45ed-97fc-de988cc572a1)

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
