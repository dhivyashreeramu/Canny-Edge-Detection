# WORKSHOP 3-Canny Edge Detection
# Name:DHIVYASHREE R
# REGNO:212225040077

## AIM

To detect edges in an image using Python and OpenCV by converting the image to grayscale, applying Gaussian blur to reduce noise, and using the Canny edge detection algorithm to identify object boundaries.

## SOFTWARE REQUIRED

* Python
* OpenCV
* Matplotlib
* Jupyter Notebook
* Anaconda (optional)

## INSTALLATION

Install the required libraries using the following command:

```bash
pip install opencv-contrib-python-headless matplotlib
```

## ALGORITHM

### Step 1: Import Libraries

* Import OpenCV for image processing.
* Import Matplotlib for displaying images.

### Step 2: Read the Image

* Load the input image `Dhanush.jpg` using `cv2.imread()`.
* Convert the image to grayscale using `cv2.IMREAD_GRAYSCALE`.

### Step 3: Apply Gaussian Blur

* Apply Gaussian blur to the grayscale image using `cv2.GaussianBlur()`.
* Use a kernel size of 5 × 5 to reduce noise and unnecessary details.

### Step 4: Perform Canny Edge Detection

* Apply the Canny edge detection algorithm using `cv2.Canny()`.
* Set the lower threshold to 50 and the upper threshold to 150.
* Detect edges and boundaries in the image.

### Step 5: Display the Results

* Create a figure using Matplotlib.
* Display the original grayscale image.
* Display the detected edges.
* Add titles and remove axis labels for clear visualization.

## PROGRAM

```python
import cv2
import matplotlib.pyplot as plt

# Read the image in grayscale
img = cv2.imread('mejpeg', cv2.IMREAD_GRAYSCALE)

# Apply Gaussian blur
blurred = cv2.GaussianBlur(img, (5, 5), 0)

# Detect edges using Canny
edges = cv2.Canny(blurred, 50, 150)

# Display original image and detected edges
plt.figure(figsize=(10, 5))

plt.subplot(121)
plt.imshow(img, cmap='gray')
plt.title('Original Image')
plt.axis('off')

plt.subplot(122)
plt.imshow(edges, cmap='gray')
plt.title('Detected Edges')
plt.axis('off')

plt.show()
```

## OUTPUT

# The following outputs are obtained:

# 1. Original image and detected edges displayed side by side.
<img width="658" height="426" alt="image" src="https://github.com/user-attachments/assets/c6fb7ef2-c31c-4796-8f46-f1c7a460a258" />


## RESULT

Thus, edge detection was successfully performed using Python, OpenCV, and Matplotlib. Gaussian blur was used to reduce image noise, and the Canny edge detection algorithm identified the edges and boundaries of objects in the image.
