# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().
### Step2
Convert the saved BGR image to RGB using cvtColor().
### Step3
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator.
### Step4
Apply the filters using cv2.filter2D() for each respective filters.
### Step5
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().
## Program:
```
Developed By   :G.Chethan Kumar
Register Number:212222240022
```
### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("groot.jpg")
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

![Screenshot from 2023-09-13 21-53-03](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/35a34f7f-efa9-4bc3-922b-1a3425fbf860)


ii) Using Weighted Averaging Filter

![Screenshot from 2023-09-13 21-53-16](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/fbdaca7d-e52f-4115-b740-69ebe2e76197)


iii) Using Gaussian Filter

![Screenshot from 2023-09-13 21-53-22](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/326b2028-0b0b-4da2-8c8f-e880c9586cdf)


iv) Using Median Filter

![Screenshot from 2023-09-13 21-53-28](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/b063f1dc-038f-46f2-bd2f-f09ff4b5511c)


### 2. Sharpening Filters

i) Using Laplacian Kernal

![Screenshot from 2023-09-13 21-53-33](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/26d818f0-eed0-4ed0-8c87-ad3adebfa795)


ii) Using Laplacian Operator

![Screenshot from 2023-09-13 21-57-57](https://github.com/Gchethankumar/IMPLEMENTATION-OF-FILTERSS/assets/118348224/505fe23d-b42b-4d25-a3fa-f488d24cfe7b)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
