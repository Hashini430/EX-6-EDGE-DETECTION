# EX-6-EDGE-DETECTION
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
```
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
<img width="617" height="462" alt="image" src="https://github.com/user-attachments/assets/eaf21062-9bb5-4ca7-9055-08c4928e0a57" />

### SOBEL EDGE DETECTION:
<img width="616" height="455" alt="image" src="https://github.com/user-attachments/assets/08d34952-d457-4146-8ee3-e5fa5833bee6" />

### LAPLACIAN EDGE DETECTOR:
<img width="615" height="455" alt="image" src="https://github.com/user-attachments/assets/ca4ed298-6019-414f-8158-bacc669c4953" />
### CANNY EDGE DETECTOR:
<img width="611" height="460" alt="image" src="https://github.com/user-attachments/assets/a6296d19-82b7-4a51-b358-7b27968fd481" />

## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
