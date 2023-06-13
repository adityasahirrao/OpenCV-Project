# OpenCV_Project
# Analyzing the size of different objects in an image using OpenCV

The provided code is an example of object dimension measurement using computer vision techniques. The code uses OpenCV and other libraries to detect objects in an image and estimate their dimensions based on a reference object of known size. The goal is to measure the width and height of various objects in the image.

The code reads an image file and performs preprocessing steps such as converting the image to grayscale and applying Gaussian blur. It then applies edge detection using the Canny algorithm to identify the contours of objects in the image.

Contours are sorted from left to right to establish a reference object. The reference object is assumed to be a square with known dimensions (in this case, a 2cm by 2cm square). The distance in pixels between two corners of the reference object is calculated, and the conversion factor between pixels and centimeters is determined.

Next, the code iterates over the remaining contours (excluding the reference object) and performs the following steps for each contour:

1. Calculates the dimensions of the object by measuring the distances between its corners.
2. Draws the bounding box around the object.
3. Calculates the width and height of the object in centimeters using the pixel-to-centimeter conversion factor.
4. Displays the dimensions next to the object.

The final result is an annotated image showing the detected objects with their respective dimensions.
