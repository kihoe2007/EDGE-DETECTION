# EXP-NO-6 EDGE-DETECTION
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
```
DEVELOPED BY : Kishore S M
REG NO : 212224231031
```
## Program :
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('kishore.jpeg')  # Replace with your image path
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
# Original Image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
<img width="1137" height="590" alt="image" src="https://github.com/user-attachments/assets/fc4c1807-d6e4-4bc9-a06d-f75f2951c32c" />

### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5)  # Sobel in x direction
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  # Sobel in y direction
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  # Combine both directions
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```
<img width="762" height="599" alt="image" src="https://github.com/user-attachments/assets/86427876-440f-4064-9c92-baf73f744104" />

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```
<img width="896" height="612" alt="image" src="https://github.com/user-attachments/assets/67abfcd9-99f9-43da-92c8-062efd1847cd" />

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```
<img width="870" height="584" alt="image" src="https://github.com/user-attachments/assets/f5ca0a11-6745-40e9-ab55-5a057dc2efb3" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
