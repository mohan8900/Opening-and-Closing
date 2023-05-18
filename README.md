# Exp no: 11
# Implementation of Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
1. Step1:
Import the necessary packages

2. Step 2:
Create the Text using cv2.putText

3. Step 3:
Create the structuring element

4. Step 4:
Use Opening operation

5. Step 5:
Use Closing Operation

6. Step 6:
end the program.
 
## Program:

``` Python
# Import the necessary packages
import numpy as np
import cv2
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((100,300),dtype='uint8')
font=cv2.FONT_HERSHEY_COMPLEX
im=cv2.putText(img1,'VISHWAK',(5,65),font,2,(255),5,cv2.LINE_AA)
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
<img width="282" alt="111" src="https://user-images.githubusercontent.com/77089276/171875818-6adfccee-4e69-4d0b-a4a4-e9bafe0d26e1.PNG">
### Display the result of Opening
<img width="280" alt="112" src="https://user-images.githubusercontent.com/77089276/171875840-e71096e6-ed5b-4878-ad13-a2a5b15fbd05.PNG">
### Display the result of Closing
<img width="275" alt="113" src="https://user-images.githubusercontent.com/77089276/171875873-63d39550-35cb-4bc0-bdba-0dcdb2372e53.PNG">

## Result:

Thus the Opening and Closing operation is used in the image using python and OpenCV.
