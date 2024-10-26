# Implementation-of-Erosion-and-Dilation->
## Aim:
To implement Erosion and Dilation using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
```
Developed By : Kabilan V
Reg No : 212222100018
```
### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "Kabilan V"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
### Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
```
### Erode the image
```
eroded_image = cv2.erode(image, kernel, iterations=1)
eroded_image_rgb = cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB)
plt.imshow(eroded_image_rgb)
plt.title("Eroded Image")
plt.axis("off")
```
### Dilate the image
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
dilated_image_rgb = cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB)
plt.imshow(dilated_image_rgb)
plt.title("Dilated Image")
plt.axis("off")
```
## Output:

### Display the input Image
![download](https://github.com/user-attachments/assets/1170d49e-ac9b-412f-b939-25ad2f5775ea)


### Display the Eroded Image
![download](https://github.com/user-attachments/assets/b42e1755-963a-4823-8072-4f5ca7381923)


### Display the Dilated Image
![download](https://github.com/user-attachments/assets/2de9f9f1-f54c-46f4-b41f-8cce6c1c4115)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
