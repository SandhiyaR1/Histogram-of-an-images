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

### Step4:
Use calcHist() function to mark the image in graph frequency for gray and color image.

### Step5:
The Histogram of gray scale image and color image is shown.


## Program:
```
# Developed By: SANDHIYA R
# Register Number: 212222230129
```
```python
import cv2
import matplotlib.pyplot as plt

# Write your code to find the histogram of gray scale image and color image channels.

gray_image=cv2.imread('bird.jpg')
color_image=cv2.imread('birdd.jpg')
plt.imshow(gray_image)
plt.show()
plt.imshow(color_image)
plt.show()

# Display the histogram of gray scale image and any one channel histogram from color image

gray_hist=cv2.calcHist([gray_image],[0],None,[256],[0,256])
color_hist=cv2.calcHist([color_image],[0],None,[256],[0,256])

plt.figure()
plt.title('Histogram')
plt.xlabel('Grayscale value')
plt.ylabel('pixel count')
plt.stem(gray_hist)
plt.show()

plt.title("Histogram")
plt.xlabel("Color Value")
plt.ylabel("Pixel Count")
plt.stem(color_hist)
plt.show()

# Write the code to perform histogram equalization of the image.

import cv2
gray_image=cv2.imread('bird.jpg',0)
gray_imageimage=cv2.resize(gray_image,(400,300))
equ = cv2.equalizeHist(gray_image)
cv2.imshow('Gray Image', gray_image)
cv2.imshow('Equalized Image', equ)
cv2.waitKey(0)
cv2.destroyAllWindows()

```
## Output:
### Input Grayscale Image and Color Image
![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/407d4294-a3f1-43f7-855d-b6d9aa8e3f6f)

![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/5cd86c00-0745-4262-a6fe-91f5f2e5ec44)



### Histogram of Grayscale Image and any channel of Color Image
![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/6d62a626-e032-4aa6-ab1e-a63a33ca8b9b)

![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/5158e76a-e99c-4931-a1fd-708cedb2a80e)


### Histogram Equalization of Grayscale Image.

![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/e182a5b1-b5df-4f4e-8cb1-5068f4cc9817)

![image](https://github.com/SandhiyaR1/Histogram-of-an-images/assets/113497571/02449913-5efd-4464-9203-03d258ade6c7)


## Result: 
Thus the histogram for finding the frequency of pixels in an image with pixel values ranging from 0 to 255 is obtained. Also,histogram equalization is done for the gray scale image using OpenCV.
