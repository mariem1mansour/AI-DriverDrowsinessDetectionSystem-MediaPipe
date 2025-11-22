# Driver Drowsiness Detection with MediaPipe

> A real-time eye blink detection system using **MediaPipe FaceMesh** to calculate the **Eye Aspect Ratio (EAR)** and alert when drowsiness is detected.  
> Built in Google Colab — perfect for drivers, gamers, or anyone needing fatigue monitoring.



---

## 🚀 Features

- ✅ Real-time EAR calculation using MediaPipe FaceMesh landmarks
- ⚠️ Alerts when eyes are closed for consecutive frames (`CONSECUTIVE_FRAMES = 10`)
- 📊 Displays live EAR value on screen
- 🎥 Saves output video with visual alerts
- 🧠 Uses classic EAR formula: `(||P1-P5|| + ||P2-P4||) / (2 * ||P0-P3||)`
- 💡 Adjustable thresholds for sensitivity

---

## 🛠️ Tech Stack

- **Python**
- **MediaPipe** (for face and eye landmark detection)
- **OpenCV** (for video processing and drawing)
- **Google Colab** (for easy execution without setup)

---

## 📥 How to Use

### 1. Open in Google Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/mariem1mansour/EyeGuard-Drowsiness-Detection-with-MediaPipe/blob/main/drowsiness_detection.ipynb)

> 🔗 Replace `mariem1mansour` with your GitHub username after pushing.

### 2. Upload a Video
Run the notebook → it will prompt you to upload a `.mp4` or `.avi` video file.

### 3. Run All Cells
The script will:
- Process each frame
- Detect face landmarks
- Calculate EAR for both eyes
- Trigger red “DROWSINESS DETECTED!” alert if EAR < threshold
- Save output video: `drowsiness_detection_fixed.mp4`

---

## 📐 Key Parameters (Adjustable)

| Parameter | Value | Description |
|----------|-------|-------------|
| `EAR_THRESHOLD` | `0.4` | Below this → eyes considered closed |
| `CONSECUTIVE_FRAMES` | `10` | Frames needed to trigger alarm |

> 🔄 Tune these values based on lighting, camera quality, or user sensitivity.

---

## 🖼️ Sample Output

Your output video will show:
- Green EAR value overlay
- Red “DROWSINESS DETECTED!” warning when eyes stay closed too long
- Landmarks drawn on face

![Sample Output](assets/sample_output.jpg)

---

## 📄 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

> 💡 *Built for educational purposes — not for production use without further testing.*
