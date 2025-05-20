# 🎚️ Interactive HSV Color Tuner

![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-orange)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![License](https://img.shields.io/badge/License-MIT-green)

Real-time HSV color range adjustment tool with interactive trackbars for computer vision applications.


## ✨ Features
- 6 adjustable trackbars (Hue/Saturation/Value)
- Real-time mask visualization
- Three display windows (Original/Mask/Result)
- Works with both images and video streams

## 🚀 Quick Start
```bash
git clone https://github.com/yourusername/hsv-color-tuner.git
cd hsv-color-tuner
pip install -r requirements.txt
python hsv_tuner.py
```
## 🛠️ Usage Guide
1.Adjust trackbars to fine-tune HSV ranges:

LH/LS/LV: Lower bounds (Hue, Saturation, Value)

UH/US/UV: Upper bounds

2.View results in real-time:

frame: Original image

mask: Binary mask

res: Filtered result

3.Press ESC to exit
## 🖼️ Custom Image Setup
Replace smarties.png with your image:

```python
frame = cv2.imread('your_image.jpg')  # Change this line
```
## 🌈 Default HSV Ranges

| Parameter    | Min | Max | Description          |
|--------------|-----|-----|----------------------|
| **Hue**      | 0   | 179 | Color type (0-179°)  |
| **Saturation**| 0   | 255 | Color purity (0-100%)|
| **Value**    | 0   | 255 | Brightness (0-100%)  |

### 🔧 Practical Notes:
1. **Hue Range**:
   - OpenCV uses 0-179 instead of 0-360°
   - Red wraps around (0-10 and 170-179)

2. **Recommended Starter Values**:
```python
# For blue objects:
lower_blue = np.array([100, 50, 50])
upper_blue = np.array([140, 255, 255])
```
3.**Conversion Help**:

```python
# Convert BGR to HSV
bgr_color = np.uint8([[[255,0,0]]])  # Blue in BGR
hsv_color = cv2.cvtColor(bgr_color, cv2.COLOR_BGR2HSV)
print(hsv_color)  # Shows corresponding HSV values
```

## 💻 Requirements
```txt
opencv-python>=4.5.0
numpy>=1.20.0
```




