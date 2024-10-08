# EX 10 OPENING AND CLOSING
## Aim
To implement Opening and Closing using Python and OpenCV.
## Software Required
1. Anaconda - Python 3.7
2. OpenCV
## Algorithm:
- Step1: Import the necessary packages
- Step2: Give the input text using cv2.putText()
- Step3: Perform opening operation and display the result
- Step4: Similarly, perform closing operation and display the result
- 
## Program:
```
Developed By: Bharathganesh S
REG.No:212222230022
``` 
# Import the necessary packages
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
```
# Create the Text using cv2.putText
```
image = np.zeros((300, 600, 3), dtype="uint8")
text = "Bharathganesh"
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, text, (50, 150), font, 2, (255, 255, 255), 3)

```
# Create the structuring element
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
```
# Use Opening operation
```
opening_image = cv2.morphologyEx(image, cv2.MORPH_OPEN, kernel)
plt.imshow(opening_image_rgb)
plt.title("Opening Operation")
plt.axis("off")
```
# Use Closing Operation
```
closing_image = cv2.morphologyEx(image, cv2.MORPH_CLOSE, kernel)
plt.imshow(closing_image_rgb)
plt.title("Closing Operation")
plt.axis("off")
```
## Output:
### Display the input Image

![WhatsApp Image 2024-10-08 at 11 50 43_e42d6262](https://github.com/user-attachments/assets/12522458-cff8-4d6c-ae8b-9c888043d215)

### Display the result of Opening
![WhatsApp Image 2024-10-08 at 11 50 51_d0361a79](https://github.com/user-attachments/assets/90b7fdc8-f412-4bb1-937d-3c10768faa4a)


### Display the result of Closing

![WhatsApp Image 2024-10-08 at 11 51 30_a417b78f](https://github.com/user-attachments/assets/331a0380-bdcb-47f0-bc42-bf12d50432b0)

## Result
Thus the Opening and Closing operation is used in the image using python and OpenCV.
