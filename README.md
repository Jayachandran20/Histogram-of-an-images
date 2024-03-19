![ex-3(hist)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/fbd4e93b-9c7c-47fe-985d-cf5236ce7120)![ex-3(hist)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/ffd241cf-4f1f-42cd-8e98-1c399747714c)# Histogram-of-an-images
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
 Developed By: M.JAYACHANDRAN
 Register Number: 212222240038
```
```python
import cv2
import matplotlib.pyplot as plt
gray_image = cv2.imread("cat1.jpg")
color_image = cv2.imread("cat2.jpg",-1)
cv2.imshow("Gray Image",gray_image)
cv2.imshow("Colour Image",color_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
```python
import numpy as np
import cv2
Gray_image = cv2.imread("cat1.jpg")
Color_image = cv2.imread("cat2.jpg")
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
gray_image = cv2.imread("cat1.jpg",0)
cv2.imshow('Grey Scale Image',gray_image)
equ = cv2.equalizeHist(gray_image)
cv2.imshow("Equalized Image",equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```







## Output:
### Input Grayscale Image and Color Image
![ex-3(colour and gray)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/f1124d02-92b1-4a64-8735-7fbef8375b82)



### Histogram of Grayscale Image and any channel of Color Image

#### Grayscale Image
![ex-3(hist)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/7e87bfa1-ea5f-4b56-8182-eb8ae10e077d)


#### Color Image
![ex-3(hist colour img)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/3b5112d8-709d-4973-8feb-4ad3a8bfe032)


### Histogram Equalization of Grayscale Image.
![ex-3(equi)](https://github.com/Jayachandran20/Histogram-of-an-images/assets/118447015/a83d2bda-9f4b-4b19-8a0e-d39e3daef6ec)




## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
