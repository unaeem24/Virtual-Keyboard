
# Virtual Keyboard Key Detection from Video using Fingertip Tracking

This project implements a **virtual keyboard detection system** that identifies key positions from a keyboard video frame and uses **skin color detection** to track fingertip positions, recognizing which key is being "hovered over" based on position and time.

---

## 📸 Features

* 🧠 Detects and clusters keyboard key boundaries from edges.
* 👆 Detects fingertips based on skin color (HSV range).
* ⌨️ Maps fingertip positions to keyboard keys using predefined layout.
* 🕒 Only registers a key "press" when the finger hovers over a key for a few frames (to avoid noise).
* 🎥 Processes video frame by frame and shows annotated output with key names.

---

## 🛠️ Technologies Used

* Python
* OpenCV
* NumPy

---

## 📁 Project Structure

```
virtual_keyboard/
│
├── main.py              # Main Python script (the one you provided)
├── sample_video.mp4     # A keyboard video used for testing (not included here)
├── README.md            # This file
```

---

## 🧪 How It Works

### 1. **Edge Detection & Rectangle Extraction**

* Uses Canny edge detection to find key boundaries.
* Filters and identifies convex 4-vertex rectangles as keyboard keys.
* Assigns each rectangle a key label from a predefined `KEY_MAP`.

### 2. **Fingertip Detection**

* Converts frame to HSV and applies threshold to isolate skin-colored areas.
* Detects top-most point from each valid contour as a fingertip.

### 3. **Hover Tracking**

* Tracks how long a finger hovers over a key.
* If a fingertip stays on the same key for ≥ 8 frames, a "press" is registered.

---

##  How to Run

1. **Install requirements:**

```bash
pip install numpy opencv-python
```

2. **Place your video file path in the script:**

```python
video_file = r"C:\path\to\your\keyboard_video.mp4"
```

3. **Run the script:**

```bash
python main.py
```

> Press `Q` while the video window is active to quit early.

---



with the correct Python syntax:

```python
if __name__ == "__main__":
```
