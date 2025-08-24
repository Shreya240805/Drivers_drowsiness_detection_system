# Driver’s Drowsiness Detection System

A real-time driver monitoring system that detects drowsiness by analyzing eye closure (using Eye Aspect Ratio) and head tilt angle via facial landmarks. When signs of drowsiness or dangerous head tilt are detected, the system sounds an audio alert to wake the driver and enhance road safety.

***

## Features

- Real-time face and eye detection using OpenCV and Dlib  
- Eye Aspect Ratio (EAR) calculation to detect prolonged eye closure  
- Head tilt angle calculation to detect if driver is leaning to one side  
- Audio alert (beep sound) triggered on drowsiness or dangerous head tilt  
- Visual feedback showing EAR, head tilt angle, and alerts on camera feed  

***

## Technologies Used

- Python 3.x  
- OpenCV  
- Dlib (with `shape_predictor_68_face_landmarks.dat`)  
- imutils  
- numpy  
- pygame (for audio alert)  
- scipy  

***

## Project Structure

```
Driver-Drowsiness-Detection/
│
├── drowsiness_detection.py              # Main detection script
├── shape_predictor_68_face_landmarks.dat # Facial landmarks model file
├── music.wav                           # Audio alert beep file
├── requirements.txt                    # Python dependencies list
├── README.md                          # Project documentation
```

***

## Installation & Setup

1. **Clone repository**  
```bash
git clone https://github.com/your-username/driver-drowsiness-detection.git
cd driver-drowsiness-detection
```

2. **Create virtual environment (optional but recommended)**  
```bash
python -m venv venv
source venv/bin/activate      # On Windows: venv\Scripts\activate
```

3. **Install dependencies**  
```bash
pip install -r requirements.txt
```

4. **Place the facial landmark model file**  
Download `shape_predictor_68_face_landmarks.dat` from the official Dlib model source if not included, and place it in the project folder.

5. **Ensure `music.wav` exists in your project folder** for the audio alert sound.

***

## Usage

Run the detection script:

```bash
python drowsiness_detection.py
```

- The webcam will start capturing video.
- The system detects facial landmarks to monitor eye aspect ratio and head tilt angle.
- If eye closure or head tilt exceeds set thresholds for continuous frames, an alert will be shown and an audio beep will play.
- Press `q` to exit the program.

***

## How It Works

- **Eye Aspect Ratio (EAR)** measures the ratio of distances between eye landmarks to detect blinking or eye closure.  
- **Head Tilt Angle** calculates the angle between nose and chin points; excessive tilt indicates drowsiness-related head lean.  
- If EAR falls below 0.25 for 20 consecutive frames or head tilt angle exceeds 15 degrees for 20 frames, an alert sounds.  
- OpenCV displays the video feed with contours on eyes, current head tilt angle, and warning messages when triggered.

***

## Dependencies (`requirements.txt`)

```
opencv-python==4.7.0.72
dlib==19.24.0
numpy==1.24.3
pygame==2.1.3
imutils==0.5.4
scipy==1.11.1
```

***

## Future Enhancements

- Add mouth aspect ratio to detect yawning.  
- Use deep learning for improved detection accuracy.  
- Integrate with vehicle control systems for automatic responses.  
- Mobile deployment with camera integration for driver monitoring.

***

## License

This project is open for educational and research use. Please give credit if you use or modify this work.
