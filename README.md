# OPENING--AND-CLOSING
## Aim:
To implement Opening and Closing using Python and OpenCV.

## Software Required:
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
### Step1:
Import the necessary packages

### Step2:
Give the input text using cv2.putText()

### Step3:
Perform opening operation and display the result

### Step4:
Similarly, perform closing operation and display the result

 
## Program:

 Python
Name: Sharika
Ref no: 212223230204
 
import cv2
import numpy as np
import matplotlib.pyplot as plt
# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Amruthavarshini', (100, 250), font, 1, (255, 255, 255), 2, cv2.LINE_AA)

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB for displaying
plt.title("Input Image with Text")
plt.axis('off')

# Opening is erosion followed by dilation
opened_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)

# Display the result of Opening
plt.imshow(cv2.cvtColor(opened_image, cv2.COLOR_BGR2RGB))  # Convert BGR to RGB
plt.title("Opening Operation")
plt.axis('off')

# Closing is dilation followed by erosion
closed_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closed_image)
plt.axis("off")


## Output:




### Display the result of Opening
<br>
<br>
<br>

![WhatsApp Image 2025-11-03 at 11 25 05_92f0393d](https://github.com/user-attachments/assets/67b7304f-db5a-434d-a196-e306e0cfe340)


<br>
<br>
<br>

### Display the result of Closing
<br>
<br>
<br>

![WhatsApp Image 2025-11-03 at 11 25 05_92f0393d](https://github.com/user-attachments/assets/158e6ea9-3eab-4ccb-9fa3-8d5e601f990c)



<br>
<br>
<br>

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
