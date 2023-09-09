# HISTOGRAM
# Histogram and Histogram Equalization of an image
## Aim
To obtain a histogram for finding the frequency of pixels in an Image with pixel values ranging from 0 to 255. Also write the code using OpenCV to perform histogram equalization.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import cv2 and matplotlib.pyplot
<br>

### Step2:
Read and display the input images
<br>

### Step3:
Calculate the Histogram Values using calcHist()
<br>

### Step4:
Display the histograms
<br>

### Step5:
Calculate and display the equalized image using equalizeHist()
<br>


## Program:
```
# Developed By: MUKESH V
# Register Number: 212222230086
```
```python
import cv2
import matplotlib.pyplot as plt

gray_image = cv2.imread('download.jpg')
color_image = cv2.imread('ok.jpg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()

# Histogram for Gray scale and Color image
hist = cv2.calcHist([gray_image],[0],None,[256],[0,256])
hist1 = cv2.calcHist([color_image],[1],None,[256],[0,256])
plt.figure()
plt.title("Histogram")
plt.xlabel('GrayScaleValue')
plt.ylabel('PixelCount')
plt.stem(hist)
plt.show()
plt.figure()
plt.title("Histogram")
plt.xlabel('Intensity Value')
plt.ylabel('PixelCount')
plt.stem(hist1)
plt.show()

# Equalized Image
Gray_image=cv2.imread('apple.jpg',0)
equ = cv2.equalizeHist(Gray_image)
cv2.imshow('Gray Image',Gray_image)
cv2.imshow('Equalized Image',equ)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/MukeshVelmurugan/HISTOGRAM/assets/118707363/2805cd6f-bc5b-4a1b-b27a-d0a99d59d5f9)

![image](https://github.com/MukeshVelmurugan/HISTOGRAM/assets/118707363/afb2d229-3718-40df-b515-ad6651d20c91)

### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/MukeshVelmurugan/HISTOGRAM/assets/118707363/903c8391-94d4-4766-a67f-a80ce28884a5)
![image](https://github.com/MukeshVelmurugan/HISTOGRAM/assets/118707363/4d48e84a-552a-40c5-94fa-c5c11e3f58ab)


### Histogram Equalization of Grayscale Image
![image](https://github.com/MukeshVelmurugan/HISTOGRAM/assets/118707363/6c8ca0ea-2246-4fbb-9555-8b1d94fd1a8f)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
