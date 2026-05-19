# Edge-Linking-using-Hough-Transformm
## Aim:
To write a Python program to detect the lines using Hough Transform.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:

Import all the necessary modules for the program.
### Step2:

Load a image using imread() from cv2 module.
### Step3:

Convert the image to grayscale.
### Step4:

Using Canny operator from cv2,detect the edges of the image.
### Step5:

Using the HoughLinesP(),detect line co-ordinates for every points in the images.Using For loop,draw the lines on the found co-ordinates.Display the image.

## Program:
### Developed by 
#### Name : Keerthivasan K S
#### Reg No : 212224230120

### Input Image:
```py
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qn_7_.jpg')  
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  
plt.title("Input Image")
plt.axis('off')
```
## Grayscale Image:
```py
plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')
```
## Canny Edge Detector:
```py
edges = cv2.Canny(gray_image, 50, 150)  
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')
```
## Result of Hough Transform:
```py
lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line[0]  
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)  
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB)) 
plt.title("Result of Hough Transform")
plt.axis('off') 
```
## Output

### Input image 
<img width="515" height="390" alt="download" src="https://github.com/user-attachments/assets/d16118cd-6381-454e-8542-d922f6b1768e" />

### grayscale image

<img width="806" height="518" alt="image" src="https://github.com/user-attachments/assets/d693492c-462b-49b1-9ea1-31de282637cd" />

### Canny Edge detector output
<img width="515" height="390" alt="download" src="https://github.com/user-attachments/assets/119c0eb6-bf4d-4f8e-a37d-98c029ca717f" />

### Display the result of Hough transform

<img width="515" height="390" alt="download" src="https://github.com/user-attachments/assets/2d3c85a0-a5f9-4208-8992-b956ba13ae63" />


## Result:
Thus, the image has been successfully converted.
