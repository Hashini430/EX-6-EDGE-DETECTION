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

### ORIGINAL IMAGE:
```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('exp-6.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title('Original Image')
plt.axis('off')
```
### SOBEL EDGE DETECTOR
```
sobel_x = cv2.Sobel(gray_image, cv2.CV_64F, 1, 0, ksize=5) 
sobel_y = cv2.Sobel(gray_image, cv2.CV_64F, 0, 1, ksize=5)  
sobel_combined = cv2.magnitude(sobel_x, sobel_y)  
plt.imshow(sobel_combined, cmap='gray')
plt.title('Sobel Edge Detection')
plt.axis('off')
```

### LAPLACIAN EDGE DETECTOR
```
laplacian = cv2.Laplacian(gray_image, cv2.CV_64F)
plt.imshow(laplacian, cmap='gray')
plt.title('Laplacian Edge Detection')
plt.axis('off')
```

### CANNY EDGE DETECTOR
```
canny_edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(canny_edges, cmap='gray')
plt.title('Canny Edge Detection')
plt.axis('off')  
```

## Output:
### ORIGINAL IMAGE:
<img width="613" height="458" alt="image" src="https://github.com/user-attachments/assets/48a33a3e-f217-4da7-8253-dfe56e886ac8" />

### SOBEL EDGE DETECTION:
<img width="612" height="456" alt="image" src="https://github.com/user-attachments/assets/a7482245-45aa-4262-9d8d-2f1201ead3c8" />

### LAPLACIAN EDGE DETECTOR:

<img width="617" height="462" alt="image" src="https://github.com/user-attachments/assets/1d8e9793-3029-446b-b693-2b602808a06d" />

### CANNY EDGE DETECTOR:
<img width="615" height="461" alt="image" src="https://github.com/user-attachments/assets/18a3711a-4a76-4c36-a8ad-3599345c6ced" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
