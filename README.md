# IMPLEMENTATION-OF-FILTERSS
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
Plot the original and filtered image by using matplotlib.pyplot

### Step5
End the program.

## Program:
```
### Developed By   :IYYANAR S
### Register Number:212222240036
```
### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("space.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
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
![61](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/687aa8bd-bb45-4fa3-8145-a39059a53f34)


ii) Using Weighted Averaging Filter
![62](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/b57a7c17-c84d-495f-a3a2-d7a7ccfe0159)


iii) Using Gaussian Filter
![63](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/4addbf3c-1a01-4303-9410-45abb234ebc8)


iv) Using Median Filter
![64](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/18aa01ac-caa6-455f-a071-59745c4ea3dc)


### 2. Sharpening Filters


i) Using Laplacian Kernal

![65](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/5f06dbfa-624c-4c35-be37-f5a4c6edae05)

ii) Using Laplacian Operator
![66](https://github.com/Iyyanar22009120/IMPLEMENTATION-OF-FILTERSS/assets/118680259/269c05ba-ef44-4107-9369-74a0fe7af596)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
