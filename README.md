# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the packages

### Step2:
create the text image

### Step3:
create the structural element  

### Step4:
use opening operation using the text and structural image

### Step5:
use closing operation using the text and structural image

 
## Program:

```
# Import the necessary packages
import cv2
import numpy as np
from matplotlib import pyplot as plt

# Create the Text using cv2.putText
img=np.zeros((100,500),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX_SMALL
img1=cv2.putText(img1,'   KARTHIKEYAN  ',(5,70),font,2,(255),5,cv2.LINE_AA)
plt.imshow(img1)
plt.title('original')
plt.axis('off')

# Create the structuring element
Kernel=cv2.getStructuringElement(cv2.MORPH_CROSS,(11,11))

# Use Opening operation
image1=cv2.morphologyEx(img1,cv2.MORPH_OPEN,Kernel)
plt.imshow(image1)
plt.title('opening')
plt.axis('off')

# Use Closing Operation
image2=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,Kernel)
plt.imshow(image2)
plt.title('opening')
plt.axis('off')

```
## Output:

### Display the input Image
![op](original.png)

### Display the result of Opening
![op](openinng.png)

### Display the result of Closing
![op](closing.png)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.