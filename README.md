# EXP-9-Implementation-of-Erosion-and-Dilation

# Implementation of Erosion and Dilation Using OpenCV

## Aim

To write a Python program using OpenCV to perform morphological operations such as Erosion and Dilation on an image.

The program performs the following operations:

- Image Erosion
- Image Dilation

## Software Used

- Anaconda – Python 3.7
- Jupyter Notebook / VS Code
- OpenCV (cv2)
- NumPy
- Matplotlib

## Algorithm

### Step 1:

Import the required libraries: OpenCV, NumPy, and Matplotlib.

### Step 2:

Create a blank image using NumPy.

### Step 3:

Insert text onto the image using OpenCV's text drawing function.

### Step 4:

Display the original image.

### Step 5:

Create a structuring element (kernel) of suitable size.

### Step 6: Image Erosion

- Apply the erosion operation using the created kernel.
- Remove pixels from the boundaries of foreground objects.
- Display the eroded image.

### Step 7: Image Dilation

- Apply the dilation operation using the same kernel.
- Add pixels to the boundaries of foreground objects.
- Display the dilated image.

### Step 8:

Compare the original, eroded, and dilated images.

## Program

## Import libraries
```
import cv2
import matplotlib.pyplot as plt
```
## Read and display the original image
```
img = cv2.imread("image.png")

plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")
plt.show()
```
## Perform Erosion
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

erosion = cv2.erode(img, kernel, iterations=1)

plt.imshow(cv2.cvtColor(erosion, cv2.COLOR_BGR2RGB))
plt.title("Image Erosion")
plt.axis("off")
plt.show()
```
## Perform Dilation
```
kernel = cv2.getStructuringElement(cv2.MORPH_RECT, (5, 5))

dilation = cv2.dilate(img, kernel, iterations=1)

plt.imshow(cv2.cvtColor(dilation, cv2.COLOR_BGR2RGB))
plt.title("Image Dilation")
plt.axis("off")
plt.show()
```
## Display all outputs together
```
plt.figure(figsize=(15, 5))

plt.subplot(1, 3, 1)
plt.imshow(cv2.cvtColor(img, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 3, 2)
plt.imshow(cv2.cvtColor(erosion, cv2.COLOR_BGR2RGB))
plt.title("Image Erosion")
plt.axis("off")

plt.subplot(1, 3, 3)
plt.imshow(cv2.cvtColor(dilation, cv2.COLOR_BGR2RGB))
plt.title("Image Dilation")
plt.axis("off")

plt.show()
```

## Developed By

**Name:** P.Bhavankumar

**Register No:** 212225240026

## Output

## Original Image

- A text image containing characters is displayed.
- The image serves as the input for morphological processing.
<img width="734" height="439" alt="image" src="https://github.com/user-attachments/assets/4381e3eb-fd5a-494d-ba40-f0bdc4df0ddc" />

## Erosion

- Original image is displayed.
- Eroded image is displayed.
- The thickness of the characters is reduced.
- Object boundaries shrink inward.
<img width="727" height="431" alt="image" src="https://github.com/user-attachments/assets/ce4f6ffb-38c7-42e5-bd51-d74fdbd43430" />

## Dilation

- Original image is displayed.
- Dilated image is displayed.
- The thickness of the characters increases.
- Object boundaries expand outward.
<img width="734" height="430" alt="image" src="https://github.com/user-attachments/assets/271a3baa-d912-4daf-974d-88b91304686b" />

## Display all outputs together
<img width="1526" height="295" alt="image" src="https://github.com/user-attachments/assets/c2c4270e-4a4d-4d9c-a5a0-13ad9a272699" />

## Result

Thus, the morphological operations **Erosion** and **Dilation** are successfully implemented using OpenCV.
