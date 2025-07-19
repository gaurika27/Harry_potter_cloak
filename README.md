# Harry_potter_cloak

A magical computer vision project that recreates Harry Potter's legendary invisibility cloak using Python and OpenCV. This project uses color detection and segmentation techniques to create the illusion of invisibility by replacing pixels of a colored cloth with the background.

![Harry Potter Cloak Demo](https://img.shields.io/badge/OpenCV-Computer%20Vision-blue?style=for-the-badge&logo=opencv)
![Python](https://img.shields.io/badge/Python-3.6+-green?style=for-the-badge&logo=python)

## 🎭 How It Works

The invisibility effect is achieved through a simple but effective image processing technique:

1. **Background Capture**: The program captures and stores the static background without any person in frame
2. **Color Detection**: Real-time detection of a specific colored cloth (typically red, green, or blue)
3. **Pixel Replacement**: Pixels matching the cloth color are replaced with corresponding background pixels
4. **Real-time Processing**: The effect is applied frame by frame to create smooth invisibility

## 🚀 Features

- **Real-time invisibility effect** using webcam
- **Color-based segmentation** for accurate cloth detection  
- **Customizable cloth colors** (red, green, blue, etc.)
- **Smooth background replacement** algorithm
- **Easy-to-use interface** with minimal setup required

## 🛠️ Prerequisites

Before running this project, make sure you have:

- Python 3.6 or higher
- A webcam
- A single-colored cloth (preferably red, green, or blue)
- Good lighting conditions
- A static background without the cloth color

## 📦 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/gaurika27/Harry_potter_cloak.git
   cd Harry_potter_cloak
   ```

2. **Install required dependencies:**
   ```bash
   pip install opencv-python
   pip install numpy
   ```

   Or install from requirements.txt (if available):
   ```bash
   pip install -r requirements.txt
   ```

## 🎯 Usage

1. **Prepare your setup:**
   - Ensure your background doesn't contain the same color as your cloth
   - Use a single-colored cloth without patterns or multiple colors
   - Set up good, even lighting

2. **Run the program:**
   ```bash
   python main.py
   # or
   python invisibility_cloak.py
   ```

3. **Follow the instructions:**
   - Stand away from the camera initially to capture the background
   - Wait for the background capture countdown
   - Put on your colored cloth and experience the magic!

4. **Controls:**
   - Press `ESC` or `q` to quit the application
   - Follow any on-screen prompts for calibration

## 🎨 Customization

### Changing the Cloak Color

You can modify the HSV color range in the code to detect different colored cloths:

```python
# Example for red color detection
lower_red = np.array([0, 120, 70])
upper_red = np.array([10, 255, 255])

# Example for green color detection  
lower_green = np.array([40, 40, 40])
upper_green = np.array([80, 255, 255])
```

### Adjusting Sensitivity

Fine-tune the color detection by modifying the HSV threshold values based on your lighting conditions and cloth material.

## 📁 Project Structure

```
Harry_potter_cloak/
├── main.py                 # Main application file
├── invisibility_cloak.py   # Core invisibility logic
├── utils.py               # Utility functions (if applicable)
├── requirements.txt       # Python dependencies
├── README.md             # Project documentation
└── demo/                 # Demo images/videos (if available)
```

## 🔧 Technical Details

### Algorithm Overview

1. **Background Subtraction**: Capture and store background frame
2. **Color Space Conversion**: Convert BGR to HSV for better color detection
3. **Morphological Operations**: Use erosion and dilation to clean up the mask
4. **Bitwise Operations**: Combine foreground and background using masks
5. **Frame Blending**: Smooth transition between visible and invisible regions

### Key OpenCV Functions Used

- `cv2.VideoCapture()` - Camera input
- `cv2.cvtColor()` - Color space conversion
- `cv2.inRange()` - Color thresholding
- `cv2.morphologyEx()` - Noise reduction
- `cv2.bitwise_and()` - Mask application

## 🎪 Demo

The invisibility cloak creates a magical effect where:
- Covered areas become transparent, showing the background
- Uncovered areas remain visible normally  
- Real-time processing maintains smooth video playback
- The effect works best with solid-colored backgrounds

## 🐛 Troubleshooting

### Common Issues and Solutions

**Issue**: Cloak detection is not working properly
- **Solution**: Adjust HSV color ranges for your specific cloth and lighting

**Issue**: Background is not stable
- **Solution**: Ensure the background is static during initial capture

**Issue**: Poor invisibility effect
- **Solution**: Improve lighting conditions and use a cloth without wrinkles

**Issue**: Application runs slowly
- **Solution**: Reduce frame resolution or optimize morphological operations

## 🎓 Learning Outcomes

This project teaches:
- Computer vision fundamentals
- Color space conversions (BGR to HSV)
- Image segmentation techniques
- Real-time video processing
- Morphological image operations
- Bitwise operations in image processing

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions

- Multiple color detection simultaneously
- GUI interface for color calibration
- Recording functionality for saving invisible videos
- Mobile app version
- Performance optimizations
- Additional morphological operations


---

⭐ **If you enjoyed this magical project, please give it a star!** ⭐

*"It is our choices, Harry, that show what we truly are, far more than our abilities."* - Albus Dumbledore
