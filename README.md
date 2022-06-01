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
Plot the images using plt.imshow.

 
## Program:
```
Developed by : Balaji N
Registeration Number:212220230006
```

``` Python
# Import the necessary packages

import cv2
import numpy as np
import matplotlib.pyplot as plt


# Create the Text using cv2.putText

text_image = np.zeros((100,440),dtype = 'uint8')
font = cv2.FONT_HERSHEY_SIMPLEX = 3
cv2.putText(text_image," Gowri",(5,70),font,2,(255),5,cv2.LINE_AA)
plt.title("Original Image")
plt.imshow(text_image,'magma')
plt.axis('off')


# Create the structuring element

kernel = cv2.getStructuringElement(cv2.MORPH_CROSS,(9,9))



# Use Opening operation

image1=cv2.morphologyEx(text_image,cv2.MORPH_OPEN,kernel)
plt.title("Opening")
plt.imshow(image1,'magma')
plt.axis('off')

# Use Closing Operation

image2=cv2.morphologyEx(text_image,cv2.MORPH_CLOSE,kernel)
plt.title("Closing")
plt.imshow(image2,'magma')
plt.axis('off')



```
## Output:

### Display the input Image
![Screenshot (200)](https://user-images.githubusercontent.com/75234946/171363578-1c2456b4-19b5-43c9-a67f-1bd3911ebcb2.png)


<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Opening
![Screenshot (201)](https://user-images.githubusercontent.com/75234946/171363800-d4450704-bc0b-4c93-a234-c10b6b2c5bc7.png)


<br>
<br>
<br>
<br>
<br>
<br>

### Display the result of Closing
![Screenshot (202)](https://user-images.githubusercontent.com/75234946/171364052-9540fbf1-2b46-451d-a3ae-9c7aa190021a.png)



<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
