# Exp 5: Implementation-of-filter
## Name: Ashwath M
## Register number: 212223230023

## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:

Step1: Import the required libraries.

Step2: Convert the image from BGR to RGB.

Step3: Apply the required filters for the image separately.

Step4: Plot the original and filtered image by using matplotlib.pyplot.

Step5: End the program.

## Program:

</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```Python
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("cat39.jpeg")
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
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
image3=cv2.filter2D(image2,-1,kernel1)
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
iv)Using Median Filter
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
i) Using Laplacian Linear Kernal
```Python
kernel2=np.array([[-1,-1,-1],[2,-2,1],[2,1,-1]])
image3=cv2.filter2D(image2,-1,kernel2)
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
</br>

i) Using Averaging Filter
</br>
</br><img width="867" height="417" alt="image" src="https://github.com/user-attachments/assets/2e8c1f1b-7836-4b6c-8938-579214ccd517" />

</br>
</br>
</br>

ii)Using Weighted Averaging Filter
</br>
</br><img width="646" height="307" alt="image" src="https://github.com/user-attachments/assets/b1a91f0c-5852-4f9d-81fe-fe5e8a436d27" />

</br>
</br>
</br>

iii)Using Gaussian Filter
</br>
</br><img width="632" height="312" alt="image" src="https://github.com/user-attachments/assets/511e66f8-2097-4392-929a-2f4719279ff7" />

</br>
</br>
</br>

iv) Using Median Filter
</br>
</br><img width="859" height="414" alt="image" src="https://github.com/user-attachments/assets/04e54b57-dc62-4d84-8e1b-5efc5dd4fe66" />

</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br><img width="633" height="303" alt="image" src="https://github.com/user-attachments/assets/e978b4e4-dac0-4029-b48e-515acd45ad2b" />

</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br><img width="652" height="313" alt="image" src="https://github.com/user-attachments/assets/d3796664-7dc1-4dfa-98f1-09c7411ea107" />

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
