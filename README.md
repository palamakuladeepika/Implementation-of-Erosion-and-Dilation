# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages to do Erosion and Dilution.
<br>


### Step2:
Create the text image of our name using putText from cv2 package.
<br>

### Step3:
Create the required structural element.
<br>

### Step4:
Apply Erode and Dilution for our NameImage.
<br>

### Step5:
Display the output images.
<br>

 
## Program:

``` Python
# Import the necessary packages

import cv2
import numpy


# Create the Text using cv2.putText

NameImage = numpy.zeros((100,1000),dtype='uint8')
font = cv2.FONT_ITALIC
cv2.putText(NameImage,'P.Deepika',(50,70),font,2,(255),5,cv2.LINE_4)
cv2.imshow("Name Image",NameImage)



# Create the structuring element

kernel1 = cv2.getStructuringElement(cv2.MORPH_CROSS,(7,7))



# Erode the image

erodeImage = cv2.erode(NameImage,kernel1)



# Dilate the image


dilationImage = cv2.dilate(NameImage,kernel1)

# Displaying the image
cv2.imshow("Name Image",NameImage)
cv2.imshow("Erode Image",erodeImage)
cv2.imshow("Dilated Image",dilationImage)





```
## Output:

### Display the input Image
![img1](https://user-images.githubusercontent.com/94154679/173018932-247ddbe7-c9e4-4b3e-a9ba-0d9ac0c6b3ed.jpg)

<br>
<br>
<br>
<br>
<br>
<br>

### Display the Eroded Image
![img2](https://user-images.githubusercontent.com/94154679/173018960-2c0ace25-d413-4d5f-984c-0a4735ab989c.jpg)

<br>
<br>
<br>
<br>
<br>
<br>

### Display the Dilated Image
![img3](https://user-images.githubusercontent.com/94154679/173018974-d238b9a7-b9c5-4fd5-8e66-25266b45fcfc.jpg)

<br>
<br>
<br>
<br>
<br>
<br>

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
