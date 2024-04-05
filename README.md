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
```
 Developed By: JOEL P
 Register Number: 212222230057
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("doggray.jpeg")
color_image = cv2.imread("vulture1.jpeg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("doggray.jpeg")
Color_image = cv2.imread("vulture1.jpeg")
import matplotlib.pyplot as plt
gray_hist = cv2.calcHist([Gray_image],[0],None,[256],[0,256])
color_hist = cv2.calcHist([Color_image],[0],None,[256],[0,256])
plt.figure()
plt.imshow(Gray_image)
plt.show()
plt.title("Histogram")
plt.xlabel("Grayscale Value")
plt.ylabel("Pixel Count")
plt.stem(gray_hist)
plt.show()
```
```python
plt.imshow(Color_image)
plt.show()
plt.title("Histogram of Color Image - Green Channel")
plt.xlabel("Intensity Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()
cv2.waitKey(0)
```
```python
import cv2
gray_image = cv2.imread("doggray.jpeg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```







## Output:
### Input Grayscale Image and Color Image

![Screenshot 2024-03-19 111438](https://github.com/AbishekAnand15/Histogram-of-an-images/assets/118706942/acd9c546-a6aa-465c-8a4e-17d24f2506a5)


### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![Screenshot 2024-03-19 111706](https://github.com/AbishekAnand15/Histogram-of-an-images/assets/118706942/a845898a-db5c-440f-a6b5-c78c66871bca)

#### Color Image
![Screenshot 2024-03-19 111828](https://github.com/AbishekAnand15/Histogram-of-an-images/assets/118706942/543636f8-140b-4f59-acfb-eb5a93acb9ce)


### Histogram Equalization of Grayscale Image.

![Screenshot 2024-03-19 111932](https://github.com/AbishekAnand15/Histogram-of-an-images/assets/118706942/2eaad6aa-e42f-4cb5-b066-bfae60fe5a6d)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
