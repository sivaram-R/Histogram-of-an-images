# Histogram-of-an-images
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Read the gray and color image using imread()

### Step2:
Print the image using imshow().

### Step3:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
### Developed By: SIVARAM R
### Register Number: 212222100050
<table>
  <tr>
    <td width=50%>
      
####  Histogram of Gray scale image and Color image  
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("flow.jpg")
color_image = cv2.imread("butter.jpg",-1)
gray_image=cv2.resize(gray_image,(400,300))
color_image=cv2.resize(color_image,(400,300))
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
#### Output:
### Input Grayscale Image and Color Image
![1](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/e7a0cec2-d5e6-40a1-88b3-bcb4cfdeb03f)
![2](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/f7deabc4-8d93-4e3b-acff-4ad1036d0f6c)
</td>
</tr>



<tr>
  <td width=50%>

### Histogram of Grayscale image and any color image
```python
import numpy as np
import cv2
gray_image = cv2.imread("flow.jpg")
color_image = cv2.imread("butter.jpg")
gray_image=cv2.resize(gray_image,(400,300))
color_image=cv2.resize(color_image,(400,300))
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
plt.imshow(color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
</td>
<td>

### Output:
#### Histogram of Grayscale image and any color image
### Grayscale image
![3](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/e73645b5-f11f-43f4-9e8a-669e26d13d69)
![4](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/0ec48348-a867-4835-9288-f87598387c59)
### Color image
![5](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/efe8a69c-3519-4be8-bc74-c3d436204d52)
![6](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/c4be3faf-0228-4751-b67e-ba96c6eb6add)
</td>
</tr>

<tr>
  <td width=50%>

### Histogram Equalization of Grayscale Image.
```python
import cv2
gray_image = cv2.imread("flow.jpg",0)
gray_image=cv2.resize(gray_image,(400,300))
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
</td>
<td>
  
### Output:
### Histogram Equalization of Grayscale Image.
![7](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/8a6c0b9a-fce8-45f9-8ba3-4adcb257e75c)
![8](https://github.com/sivaram-R/Histogram-of-an-images/assets/121165794/44d8d033-5200-4f99-a53a-711345e21ee3)
</td>
</tr>
</table>

## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
