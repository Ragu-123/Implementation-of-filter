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
### Developed By   :RAGUNATH R
### Register Number:212222240081


### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('liberty.jpeg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel = np.ones((11,11), np. float32)/121
image3 = cv2.filter2D(image2, -1, kernel)

plt.figure(figsize=(9,9))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title('Orignal')
plt.axis('off')

plt.subplot(1,2,2)
plt.imshow(image3)
plt.title('Filtered')
plt.axis('off')
```

ii) Using Weighted Averaging Filter

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('liberty.jpeg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
image4 = cv2.filter2D(image2, -1, kernel2)
plt.imshow(image4)
plt.title('Weighted Averaging Filtered')
```

iii) Using Gaussian Filter

```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image1 = cv2.imread('liberty.jpeg')
image2 = cv2.cvtColor(image1, cv2.COLOR_BGR2RGB)

gaussian_blur = cv2.GaussianBlur(src=image2, ksize=(11,11), sigmaX=0, sigmaY=0)
plt.imshow(gaussian_blur)
plt.title(' Gaussian Blurring Filtered')

```

iv) Using Median Filter

```

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

### 1.Smoothing Filters

i)Averaging filter
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/cce56f51-d15c-43a8-bf9b-4ff973ee8a27)

ii)weighted average filter
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/e3372eb8-1be2-4660-ae93-cc5b362077ac)

iii)Guassian blurring filter
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/7e2d5898-e08f-47b8-b840-e7a012740093)

iv)Median blurring filter
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/50487471-948a-48ec-bce8-729d0bd8d779)








### 2.Sharpening Filters

i) Using Laplacian Kernal
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/830e23e5-6807-4817-b82d-3eab7d43b765)


ii) Using Laplacian Operator
![image](https://github.com/Ragu-123/Implementation-of-filter/assets/113915622/160651c1-f780-425b-8a57-fc8a543c7818)


## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
