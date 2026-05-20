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
#### Name : K S Vinay Suhirthan
#### Reg No : 212224230305

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
<img width="512" height="386" alt="image" src="https://github.com/user-attachments/assets/e9e75409-48f9-4c5e-b259-1f9570da3060" />

### grayscale image
<img width="501" height="382" alt="image" src="https://github.com/user-attachments/assets/ed1fb5a4-46f0-4b62-a5ad-8e2cee2cf4ca" />

### Canny Edge detector output
<img width="512" height="390" alt="image" src="https://github.com/user-attachments/assets/14592089-8d3d-47b5-be10-bb61575c1bfe" />

### Display the result of Hough transform
<img width="512" height="397" alt="image" src="https://github.com/user-attachments/assets/77922f2f-a88e-4e46-8b6d-6e72fdb5937b" />


## Result:
Thus, the image has been successfully converted.
