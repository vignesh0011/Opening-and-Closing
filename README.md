### EX NO : 11
### DATE  : 17.05.2023
# <p align="center">Opening and Closing</p>

## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step 1:
Import the necessary packages
### Step 2:
Read the image
### Step 3:
Create the structuring element
### Step 4:
Use Opening operation
### Step 5:
Use Closing Operation
### Step 6:
Display all the output images

 
## Program:

``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt
from google.colab.patches import cv2_imshow

# Create the Text using cv2.putText
img1=np.zeros((300,500),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"VM",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2_imshow(img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(6,6))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2_imshow(img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2_imshow(img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
## Output:

### Display the input Image
![image](https://github.com/vignesh0011/Opening-and-Closing/assets/53014593/1541aa3f-2b3f-420b-bb58-974999464bf3)
<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Opening
![image](https://github.com/vignesh0011/Opening-and-Closing/assets/53014593/1500ca18-e202-44eb-a54a-d52f0cd439c9)
<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
![image](https://github.com/vignesh0011/Opening-and-Closing/assets/53014593/b4170e62-db93-4d96-b812-f954fdd9878e)
<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
