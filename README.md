# IMPLEMENTATION OF EROSION AND DILATION
## AIM:
To implement Erosion and Dilation using Python and OpenCV.
## SOFTWARE REQUIRED:
1. Anaconda - Python 3.7
2. OpenCV
## ALGORITHM:
### Step 1:
Import the necessary packages.
### Step 2:
Create the Text using cv2.putText
### Step 3:
Create the structuring element.
### Step 4:
Erode the image.
### Step 5:
Dilate the image.

## PROGRAM:
```
/*
Developed by   : SAFA
Register Number: 212220230040
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_ITALIC
cv2.putText(img1,'SAFA',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.axis('off')
plt.imshow(img1)
plt.show()

# Create the structuring element
kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))

# Erode the image
image_erode1=cv2.erode(img1,kernel)
plt.axis('off')
plt.imshow(image_erode1)
plt.show()

# Dilate the image
image_dilate1=cv2.dilate(img1,kernel)
plt.axis('off')
plt.imshow(image_dilate1)
plt.show()
```
## Output:

### Display the input Image
![10a](https://user-images.githubusercontent.com/75234912/171090705-8d5f285e-69b3-4e8f-94c1-3f364d29d85c.png)


### Display the Eroded Image
![10b](https://user-images.githubusercontent.com/75234912/171090714-a6c22d96-be3d-498e-a3f7-8631ecb4fa62.png)


### Display the Dilated Image
![10c](https://user-images.githubusercontent.com/75234912/171090720-662c4c7b-3301-4588-bed9-0b00533b59d4.png)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
