# Virtual-Sunglasses-Try-On-using-OpenCV
This is a fun project that adds sunglasses to photos using image processing

## Overview

This project demonstrates how to overlay a sunglasses image onto a human face using OpenCV in Python. It focuses on basic image manipulation techniques such as resizing, region-of-interest (ROI) selection, and pixel replacement.

The implementation is intentionally simple and serves as a foundational exercise for understanding how image compositing works before moving on to more advanced techniques like alpha blending and facial landmark detection.

---

## Features

* Load and process images using OpenCV
* Resize overlay image to fit a target region
* Replace a specific region of an image (eye area)
* Basic image visualization using Matplotlib

---

## Project Structure

```
.
├── main_sunglass.ipynb
├── face image (input)
├── sunglasses image (PNG)
└── README.md
```

---

## Requirements

Make sure the following libraries are installed:

```bash
pip install opencv-python numpy matplotlib
```

---

## How It Works

1. The face image is loaded
2. The sunglasses image is resized to match the desired region
3. A region of interest (ROI) is selected on the face image
4. The resized sunglasses image is placed onto that region

---

## Example Code Snippet

```python
import cv2
import matplotlib.pyplot as plt

# Resize sunglasses
glassPNG = cv2.resize(glassPNG, (110, 35))

# Copy original image
faceWithGlassesNaive = faceImage.copy()

# Define region
y1, x1 = 300, 200
h, w = glassPNG.shape[:2]

# Overlay
faceWithGlassesNaive[y1:y1+h, x1:x1+w] = glassPNG

# Display
plt.imshow(faceWithGlassesNaive[..., ::-1])
plt.axis('off')
```

---

## Output
<img width="444" height="555" alt="image" src="https://github.com/user-attachments/assets/eca38fe0-9848-4d7e-8799-f1aa62b8d288" />

<br>
<img width="1450" height="157" alt="image" src="https://github.com/user-attachments/assets/80060d81-e475-4b6d-9882-dbf8af6142a7" />

<br>
The final output is an image where the sunglasses are placed over the eye region of the face.
<br>
<img width="1452" height="928" alt="image" src="https://github.com/user-attachments/assets/4f42c1b2-d84a-4174-9d41-9a4de88bfced" />





---

## Future Improvements

* Integrate face and eye detection using Haar cascades or Dlib
* Add alpha blending for realistic overlays
* Dynamically scale and position glasses based on facial landmarks
* Support multiple face inputs

---

## License

This project is open-source and available for educational purposes.
