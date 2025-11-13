# Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
import the neccesary packages
### Step2:
Create the text using cv2.put Text
### Step3:
create the structuting element
### Step4:
Erodde the image
### Step5:
Dilate the image

 
## Program:

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt
def load_image():
    blank_image = np.zeros((400,800))
    font = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_image,text='VAYLOR',org=(120,250),fontFace=font,fontScale = 5,color=(255,255,255),thickness=15,lineType=cv2.LINE_AA)
    return blank_image
def display_img(img):
    fig = plt.figure(figsize=(12,10))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    plt.show()
img=load_image()
display_img(img)
kernel=np.ones((5,5),dtype=np.uint8)
erosion = cv2.erode(img,kernel,iterations = 2)
display_img(erosion)
dilution=cv2.dilate(img,kernel,iterations=2)
display_img(dilution)

```
## Output:

### Display the input Image

<img width="1258" height="655" alt="image" src="https://github.com/user-attachments/assets/cb029586-a421-49d4-aa33-1973f44a050e" />

### Display the Eroded Image

<img width="1270" height="658" alt="image" src="https://github.com/user-attachments/assets/9b1e7729-5aaa-44bf-af8e-69e76eaac217" />

### Display the Dilated Image
<img width="1266" height="645" alt="image" src="https://github.com/user-attachments/assets/c2a68740-cd0c-4ffe-9080-c45497bb824e" />



## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
