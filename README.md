
# 📏 Object Size Measurement using OpenCV

This project implements an **automated object dimension measurement system** using **OpenCV** and **image processing techniques**. By leveraging contour detection and a reference object, the system accurately determines the **real-world dimensions (width & height)** of objects present in an image.

## 🔥 Features
- 📸 **Preprocesses images** using **grayscale conversion, Gaussian blur, and edge detection** (Canny algorithm).
- 🔍 **Detects contours** and sorts them based on position to identify the reference object.
- 🎯 **Pixel-to-CM calibration** using a known **2cm x 2cm square** as the reference.
- 📏 **Computes object dimensions** using Euclidean distance and conversion factors.
- 🖼 **Overlays measured dimensions** on the image with bounding boxes.

## 🛠️ Tech Stack
- **Python**
- **OpenCV**
- **NumPy**
- **Scipy**
- **Imutils**

## 🚀 How It Works
1. **Preprocess Image**  
   - Convert to grayscale  
   - Apply Gaussian blur  
   - Perform edge detection (Canny)  

2. **Find Contours**  
   - Extract contours using `cv2.findContours()`  
   - Sort contours left-to-right to identify the **reference object**  

3. **Compute Pixel-to-CM Ratio**  
   - Extract the bounding box of the reference square  
   - Calculate the **pixel-to-cm conversion factor**  

4. **Measure Object Dimensions**  
   - Extract bounding boxes of other objects  
   - Compute width & height using Euclidean distance  
   - Convert pixel values to centimeters  

5. **Overlay Measurements**  
   - Draw bounding boxes  
   - Annotate image with **measured dimensions**  

## 📷 Example Output
The final image displays detected objects **with their real-world dimensions**.

## 🏗️ Setup Instructions
1. **Install Dependencies**  
   ```bash
   pip install numpy opencv-python scipy imutils
   ```
2. **Run the Script**  
   ```bash
   python image.py
   ```
3. **Provide an Image** (`12.jpg`) with a **2cm reference square**.

## 📌 Notes
- A **fixed-size reference object** is required in the image.
- Ensure the **background contrast** is sufficient for edge detection.

