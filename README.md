# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

### Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

### Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

    Translation moves the image along the x or y-axis.
    Scaling resizes the image by scaling factors.
    Shearing distorts the image along one axis.
    Reflection flips the image horizontally or vertically.
    Rotation rotates the image by a given angle.


### Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

### Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.
## Program:
```python
Developed By: ANANDHAMOORTHY.K
Register Number: 212222100004

import cv2
import numpy as np
import matplotlib.pyplot as plt

# Load the image
image = cv2.imread('tarantino.jpg')
i)Image Translation
rows, cols, _ = image.shape
M_translate = np.float32([[1, 0, 50], [0, 1, 100]])  # Translate by (50, 100) pixels
translated_image = cv2.warpAffine(image_rgb, M_translate, (cols, rows))

# Plot the original and transformed images
plt.figure(figsize=(12, 8))

plt.subplot(2, 3, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis('off')

ii) Image Scaling
scaled_image = cv2.resize(image_rgb, None, fx=1.5, fy=1.5, interpolation=cv2.INTER_LINEAR)  # Scale by 1.5x


plt.subplot(2, 3, 3)
plt.imshow(scaled_image)
plt.title("Scaled Image")
plt.axis('off')




iii)Image shearing
M_shear = np.float32([[1, 0.5, 0], [0.5, 1, 0]])  # Shear with factor 0.5
sheared_image = cv2.warpAffine(image_rgb, M_shear, (int(cols * 1.5), int(rows * 1.5)))

plt.subplot(2, 3, 4)
plt.imshow(sheared_image)
plt.title("Sheared Image")
plt.axis('off')




iv)Image Reflection
reflected_image = cv2.flip(image_rgb, 1)  # Horizontal reflection (flip along y-axis)

plt.subplot(2, 3, 5)
plt.imshow(reflected_image)
plt.title("Reflected Image")
plt.axis('off')


v)Image Rotation
M_rotate = cv2.getRotationMatrix2D((cols / 2, rows / 2), 45, 1)  # Rotate by 45 degrees
rotated_image = cv2.warpAffine(image_rgb, M_rotate, (cols, rows))

plt.subplot(2, 3, 6)
plt.imshow(rotated_image)
plt.title("Rotated Image")
plt.axis('off')







vi)Image Cropping
cropped_image = image_rgb[50:300, 100:400]  # Crop a portion of the image

plt.imshow(cropped_image)
plt.title("Cropped Image")
plt.axis('off')
plt.show()



```
## Output:
### i)Image Translation
![Screenshot 2024-10-01 110140](https://github.com/user-attachments/assets/b3bd5a4c-5e99-407f-b94c-9abfd9c8d286)


### ii) Image Scaling
![Screenshot 2024-10-01 110149](https://github.com/user-attachments/assets/c619eecc-80a1-4daf-a13e-d7a2ef8ec0d1)



### iii)Image shearing
![Screenshot 2024-10-01 110159](https://github.com/user-attachments/assets/e93cbe73-25d6-4b72-9b2e-acb275a21666)



### iv)Image Reflection
![Screenshot 2024-10-01 110209](https://github.com/user-attachments/assets/bf14f4b8-b170-4441-8de3-f6e1a495187c)




### v)Image Rotation
![Screenshot 2024-10-01 110228](https://github.com/user-attachments/assets/a410aff7-8290-43f0-9961-daa33b8fd08c)




### vi)Image Cropping
![Screenshot 2024-10-01 110219](https://github.com/user-attachments/assets/8046bc70-e1f3-4ac2-8a7f-3358d971f2fa)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
