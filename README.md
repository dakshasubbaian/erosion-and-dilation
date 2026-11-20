# EX. No: 9 – IMPLEMENTATION OF EROSION AND DILATION

## Developed by:
## Name: DAKSHA SUBBAIAN
## Register number:212223230036

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

## Software Required

1. Anaconda – Python 3.7
2. OpenCV
3. NumPy
4. Matplotlib

## Algorithm

### Step 1:
Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:
Create a blank black image of size 500 × 500 using NumPy.

### Step 3:
Insert the text "Hello World" onto the image using OpenCV's `cv2.putText()` function.

### Step 4:
Display the original input image containing the text.

### Step 5:
Create a 3 × 3 square structuring element (kernel) using NumPy.

### Step 6: Erosion
Apply the erosion operation using `cv2.erode()` to shrink the boundaries of the foreground objects.

### Step 7: Dilation
Apply the dilation operation using `cv2.dilate()` to expand the boundaries of the foreground objects.

### Step 8:
Display and compare the original, eroded, and dilated images.

## Program

```python
# EX. No: 9 - IMPLEMENTATION OF EROSION AND DILATION
# Developed by:
# Name: DAKSHA SUBBAIAN
# Register number: 212223230036

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Create a blank image
image = np.zeros((500, 500, 3), dtype=np.uint8)

# Add text on the image using cv2.putText
font = cv2.FONT_HERSHEY_SIMPLEX
cv2.putText(image, 'Hello World', (100, 250), font, 1,
            (255, 255, 255), 2, cv2.LINE_AA)

# Display the input image
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Input Image with Text")
plt.axis('off')

# Create a simple square kernel (3x3)
kernel = np.ones((3, 3), np.uint8)

# Apply erosion (shrinking effect)
eroded_image = cv2.erode(image, kernel, iterations=1)

# Display the eroded image
plt.figure()
plt.imshow(cv2.cvtColor(eroded_image, cv2.COLOR_BGR2RGB))
plt.title("Eroded Image")
plt.axis('off')

# Apply dilation (expanding effect)
dilated_image = cv2.dilate(image, kernel, iterations=1)

# Display the dilated image
plt.figure()
plt.imshow(cv2.cvtColor(dilated_image, cv2.COLOR_BGR2RGB))
plt.title("Dilated Image")
plt.axis('off')

plt.show()
```

## Output

<img width="481" height="503" alt="image" src="https://github.com/user-attachments/assets/080520ba-6758-40cc-9176-4c4f31972f65" />

<img width="486" height="510" alt="image" src="https://github.com/user-attachments/assets/84262819-6212-4a43-9aae-f8a84365169c" />

<img width="485" height="510" alt="image" src="https://github.com/user-attachments/assets/2ad95dd7-c5c2-4938-b7f9-7707dc6e0c28" />


## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using Python and OpenCV.
