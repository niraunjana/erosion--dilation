# EX 09 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:

### Step1:
Import the necessary packages

### Step2:
Insert the text using cv2.putText()

### Step3:
The perform the erosion for given text and display the text using imshow()

### Step4:
 Next,perform dilation for inout text and display the result


 
## Program:

```
Developed by : NIRAUNJANA GAYATHRI G R
Reg No : 212222230096
```

### Import the necessary packages
```
import cv2
import numpy as np 
import matplotlib.pyplot as plt
```

### Create the Text using cv2.putText
```
img1=np.zeros((100,400),dtype='uint8')
font=cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(img1,'Niraunjana',(5,70),font,2,(255),5,cv2.LINE_AA)
```

### Create the structuring element
```
kernel=np.ones((5,5),np.uint8)
kernel1=cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))
```

### Erode the image
```
image_erode1=cv2.erode(img1,kernel1)
plt.imshow(image_erode1)
plt.axis("off")
```

### Dilate the image
```
image_dilate1=cv2.dilate(img1,kernel1)
plt.imshow(image_dilate1)
plt.axis("off")
```

## Output:

### Display the input Image

![image](https://github.com/niraunjana/erosion--dilation/assets/119395610/2e6f5578-e449-4215-a5d7-f3b98a7fdc83)


### Display the Eroded Image

![image](https://github.com/niraunjana/erosion--dilation/assets/119395610/99b7f9d4-a3a8-4f02-b46c-dbee7abb7f1e)


### Display the Dilated Image

![image](https://github.com/niraunjana/erosion--dilation/assets/119395610/5a169850-779f-4551-9223-ba12110a6ebb)


## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
