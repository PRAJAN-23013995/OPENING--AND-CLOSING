# OPENING--AND-CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.

## Software Required
1. Anaconda - Python 3.7
2. OpenCV

## Algorithm:
### Step1:
Import the necessary packages.

### Step2:
Create the Text using cv2.putText.

### Step3:
Create the structuring element.

### Step4:
Use Opening operation.

### Step5:
Use Closing Operation.

## Program:
### Name: PRAJAN P
### Register Number: 212223240121

``` Python
import numpy as np
import cv2
import matplotlib.pyplot as plt

def load_img():
    blank_img = np.zeros((300,700), dtype=np.uint8)
    front = cv2.FONT_HERSHEY_SIMPLEX
    cv2.putText(blank_img, text='RAKSHI', org=(50,200), fontFace=front, 
                fontScale=5, color=(255, 255, 255), thickness=25, lineType=cv2.LINE_AA)
    return blank_img

def display_img(img,title="Original Image"):
    fig=plt.figure(figsize=(10,8))
    ax=fig.add_subplot(111)
    ax.imshow(img,cmap='gray')
    ax.set_title(title, fontsize=16)
    plt.show()

img = load_img()
display_img(img)
kernel = cv2.getStructuringElement(cv2.MORPH_CROSS, (12,12))

image=load_img()
opening_img = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
display_img(opening_img,"Opening Image")

image=load_img()
closing_img = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
display_img(closing_img,"Closing Image")

```
## Output:

### Display the input Image

![download](https://github.com/user-attachments/assets/d08dcd13-b73e-4af6-ad92-216e714c2fb1)

### Display the result of Opening

![download](https://github.com/user-attachments/assets/782750e0-dd26-46d1-ada5-c73b8df208ad)

### Display the result of Closing

![download](https://github.com/user-attachments/assets/92f7ed7c-9028-4b5c-8e31-1e47ca2a04b3)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
