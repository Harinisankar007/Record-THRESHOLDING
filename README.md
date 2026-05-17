# Record-THRESHOLDING
## Name : Harini S
## Reg no: 212224240049
## Exp no : 08

## Aim
To segment the image using Global Thresholding, Adaptive Thresholding, and Otsu’s Thresholding techniques using Python and OpenCV.

## Algorithm
Step 1: Import the required libraries such as OpenCV, NumPy, and Matplotlib.

Step 2: Read the input image using cv2.imread() and convert it into grayscale using cv2.cvtColor().

Step 3: Display the original image.

Step 4: Apply Global Thresholding using cv2.threshold() to segment the image.

Step 5: Apply Adaptive Thresholding using cv2.adaptiveThreshold() to segment the image based on neighborhood pixel values.

Step 6: Apply Otsu’s Thresholding using cv2.threshold() with THRESH_OTSU to automatically determine the optimal threshold value.

Step 7: Display the outputs of Global Thresholding, Adaptive Thresholding, and Otsu’s Thresholding.

Step 8: Show all the segmented images using Matplotlib.

## Program
## Read the image and convert to grayscale
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qn8_thresholding.tif') 
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.subplot(2, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert from BGR to RGB for display
plt.title("Original Image")
plt.axis('off')
```
##  Use Global Thresholding to segment the image
```
_, global_thresholded = cv2.threshold(gray_image, 127, 255, cv2.THRESH_BINARY)
plt.subplot(2, 2, 2)
plt.imshow(global_thresholded, cmap='gray')
plt.title("Global Thresholding")
plt.axis('off')
```
##  Use Adaptive Thresholding to segment the image
```
adaptive_thresholded = cv2.adaptiveThreshold(gray_image, 255, cv2.ADAPTIVE_THRESH_GAUSSIAN_C
plt.subplot(2, 2, 3)
plt.imshow(adaptive_thresholded, cmap='gray')
plt.title("Adaptive Thresholding")
plt.axis('off')
```
## Use Otsu's method to segment the image
```
_, otsu_thresholded = cv2.threshold(gray_image, 0, 255, cv2.THRESH_BINARY + cv2.THRESH_OTSU)
plt.subplot(2, 2, 4)
plt.imshow(otsu_thresholded, cmap='gray')
plt.title("Otsu's Method")
plt.axis('off')

```
## Display the images
```
plt.tight_layout()
plt.show()
```
## Output
## Original image
<img width="570" height="245" alt="image" src="https://github.com/user-attachments/assets/a8925f19-e927-4c35-ab7d-c672cf7923de" />

## Global , Adaptive, Otsu's Thersholding 
<img width="605" height="478" alt="image" src="https://github.com/user-attachments/assets/590897a9-e9f4-4951-9aa1-5e9e16654452" />



## Result
Thus, the image segmentation using Global Thresholding, Adaptive Thresholding, and Otsu’s Thresholding was implemented successfully using Python and OpenCV. The grayscale image was segmented using different thresholding techniques, and the segmented outputs were displayed successfully.

