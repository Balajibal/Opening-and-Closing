# Opening-and-Closing

## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the text image using cv2.putText.

### Step3:
Then create the structuring element for opening and closing.

### Step4:
Apply erosion and dilation using cv2.MORPH_OPEN and cv2.MORPH_CLOSE.

### Step5:
Show the images using cv2.imshow().
 
## Program:
```
/*
Developed by   : Balaji N
Register Number: 212220230006
*/
```
``` Python
# Import the necessary packages
import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create the Text using cv2.putText
img1=np.zeros((300,800),dtype='uint8')
font=cv2.FONT_ITALIC
img2=cv2.putText(img1,"Dineshkumar V",(5,70),font,3,(255,0,0),5,cv2.LINE_AA)
cv2.imshow("Original",img2)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Create the structuring element
kernel1=cv2.getStructuringElement(cv2.MORPH_RECT,(21,21))
kernel2=cv2.getStructuringElement(cv2.MORPH_RECT,(9,9))

# Use Opening operation
img4=cv2.morphologyEx(img1,cv2.MORPH_OPEN,kernel2)
cv2.imshow("Opening",img4)
cv2.waitKey(0)
cv2.destroyAllWindows()

# Use Closing Operation
img3=cv2.morphologyEx(img1,cv2.MORPH_CLOSE,kernel1)
cv2.imshow("Closing",img3)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## Output:
### Display the input Image
![Screenshot (200)](https://user-images.githubusercontent.com/75234946/175253136-83f268e0-2f98-442d-9d70-0a0fbf81c6fc.png)



### Display the result of Opening
![Screenshot (201)](https://user-images.githubusercontent.com/75234946/175253226-666d73c6-fba5-426b-ae0a-60179f3e81f1.png)



### Display the result of Closing
![Screenshot (202)](https://user-images.githubusercontent.com/75234946/175253299-97ef89c1-02c1-48fe-9dd5-ce018da40abd.png)



## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
