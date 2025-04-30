# THRESHOLDING
## Aim
To segment the image using global thresholding, adaptive thresholding and Otsu's thresholding using python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm

### Step1:
Import required libraries.

### Step2:
Read the image and convert it to grayscale then display it.

### Step3:
Use Global thresholding to segment the image

### Step4:
Use Adaptive thresholding to segment the image

### Step5:
Use Otsu's method to segment the image

### Step6:
End the program.

## Program
#### DEVELOPED BY:MARINO SARISHA T
#### REG NO:21223240084
```python
# Load the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Read the Image and convert to grayscale

image = cv2.imread('house.png')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(image)
plt.title('Original Image')


# Use Global thresholding to segment the image
ret_global, th_global = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)


# Use Adaptive thresholding to segment the image
th_adaptive = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C,cv2.THRESH_BINARY, 11, 2)

# Use Otsu's method to segment the image 
ret_otsu, th_otsu = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)


# Display the results
plt.imshow(th_global, cmap='gray')
plt.title('Global Thresholding (v=127)')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_adaptive, cmap='gray')
plt.title('Adaptive Gaussian Thresholding')
plt.xticks([]), plt.yticks([])
plt.show()

plt.imshow(th_otsu, cmap='gray')
plt.title("Otsu's Thresholding")
plt.xticks([]), plt.yticks([])
plt.show()
```
## Output

### Original Image
![Screenshot 2025-04-30 150542](https://github.com/user-attachments/assets/85ee772d-7d2f-4efc-a677-058069ecaa0f)

### Global Thresholding
![Screenshot 2025-04-30 150549](https://github.com/user-attachments/assets/aea9112c-3586-4713-95b7-8341c620fc70)

### Adaptive Thresholding
![Screenshot 2025-04-30 150556](https://github.com/user-attachments/assets/f1d26132-d8ed-4ce2-8250-b9a9f1ae21b4)

### Optimum Global Thesholding using Otsu's Method
![Screenshot 2025-04-30 150602](https://github.com/user-attachments/assets/9e80920d-39c6-4780-bd9a-f651c3239273)


## Result
Thus the images are segmented using global thresholding, adaptive thresholding and optimum global thresholding using python and OpenCV.
