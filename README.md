### EXP-9 Implementation-of-Erosion-and-Dilation
## Aim
To implement Erosion and Dilation using Python and OpenCV.

## Software Required
Anaconda - Python 3.7
OpenCV

## Algorithm:
### Step1:
Import the necessary pacakages

### Step2:
Create the text using cv2.putText

### Step3:
Create the structuring element

### Step4:
Erode the image

### Step5:
Dilate the Image

## Program:
#### Name: GANESH D
#### Reg.No: 212223240035

### Import the necessary packages
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
```
### Create a blank image
```
image = np.zeros((500, 500, 3), dtype=np.uint8)
```

### Add Text on the image using cv2.putText
```
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'NAME : GANESH D', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)
```

### Display the input image
```
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')
```
<img width="569" height="607" alt="image" src="https://github.com/user-attachments/assets/3b422c6d-de27-4fae-9aa3-c4f202d3358b" />

### Create a simple square kernel (3x3)
```
kernel = np.ones((3, 3), np.uint8)
```
### Apply erosion (shrinking effect)
```
eroded_image = cv2.erode(image, kernel, iterations=1)
```

### Display the eroded image
```
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Eroded Image")
plt.axis('off')
```
<img width="575" height="595" alt="image" src="https://github.com/user-attachments/assets/cc852867-2f0d-41a2-8098-7a006ec1f4cb" />

### Apply dilation (expanding effect)
```
dilated_image = cv2.dilate(image, kernel, iterations=1)
```

### Display the dilated image
```
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Dilated Image")
plt.axis('off')
```

<img width="574" height="605" alt="image" src="https://github.com/user-attachments/assets/b60c46d7-a49e-47e3-b2e3-17133b130f12" />

## Result
Thus the generated text image is eroded and dilated using python and OpenCV.
