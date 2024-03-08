# Implementation-of-filter
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import the required libraries.


### Step2
Convert the image from BGR to RGB.


### Step3
Apply the required filters for the image separately.


### Step4
Plot the original and filtered image by using matplotlib.pyplot.


### Step5
End the program.


## Program:
### Developed By   : VINOD KUMAR S
### Register Number: 212222240116
### 1. Smoothing Filters

i) Using Averaging Filter
```Python

import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("eiffle.jpg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/169
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()

```
ii) Using Weighted Averaging Filter
```Python
kernel1=np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image3=cv2.filter2D(image2,-1,kernel1)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Weighted Average Filter Image")
plt.axis("off")
plt.show()




```
iii) Using Gaussian Filter
```Python

gaussian_blur=cv2.GaussianBlur(image2,(33,33),0,0)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Blur")
plt.axis("off")
plt.show()



```

iv) Using Median Filter
```Python

median=cv2.medianBlur(image2,13)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Blur")
plt.axis("off")
plt.show()



```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```Python

kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Laplacian Kernel")
plt.axis("off")
plt.show()



```
ii) Using Laplacian Operator
```Python


laplacian=cv2.Laplacian(image2,cv2.CV_64F)
plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian)
plt.title("Laplacian Operator")
plt.axis("off")
plt.show()


```

## OUTPUT:
### 1. Smoothing Filters
i) Using Averaging Filter

![Screenshot 2024-03-08 155538](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/94067f2c-2d8e-4965-b54d-c0f3ded680c1)

ii) Using Weighted Averaging Filter

![Screenshot 2024-03-08 155605](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/c2533034-acc6-4131-91e8-49644c82dace)

iii) Using Gaussian Filter

![Screenshot 2024-03-08 155913](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/10cb7930-c2e1-433d-b7e1-020631b98f17)

iv) Using Median Filter

![Screenshot 2024-03-08 155936](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/dac8abfe-606b-4f7c-9e93-1a9ab0b0a965)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot 2024-03-08 155955](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/70e772fa-a2c5-46e7-b87f-2c3f56becb55)

ii) Using Laplacian Operator

![Screenshot 2024-03-08 160015](https://github.com/vinodkumar-s/Implementation-of-filter/assets/113497226/dcbc8a0c-ef89-44d2-837a-158b0e5ad966)

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
