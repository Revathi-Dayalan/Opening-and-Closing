# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
<br>
Import the necessary packages.


### Step2:
<br>
Create the Text using cv2.putText

### Step3:
<br>
Create the structuring element

### Step4:
<br>
Use Opening operation

### Step5:
<br>
Use Closing Operation

### Step6:
<br>
End the program

 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'REVATHI',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(im)

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(im,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)

# Use Closing Operation
image1=cv2.morphologyEx(im,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image1)


















```
## Output:

### Display the input Image
![REV1](https://user-images.githubusercontent.com/96000574/175560193-4c8a3082-4cac-4ab3-ab8a-8b89b4def03b.png)


### Display the result of Opening
![REV2](https://user-images.githubusercontent.com/96000574/175560238-0334ae9f-377d-4362-96fe-0eb0b6468b07.png)


### Display the result of Closing
![REV3](https://user-images.githubusercontent.com/96000574/175560273-21ae42e4-4da9-4946-998c-b6549cc5c378.png)


## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
