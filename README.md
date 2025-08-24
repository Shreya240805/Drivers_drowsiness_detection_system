# Driver’s Drowsiness Detection System

A real-time computer vision system to detect driver drowsiness by monitoring eye closure and head tilt using OpenCV and Dlib. The system alerts the driver with a beep sound when signs of drowsiness are detected to improve driving safety.

***

## Features

- Real-time face and eye detection with OpenCV and Dlib
- Eye Aspect Ratio (EAR) calculation to detect eye closure
- Head tilt detection to identify if the driver is leaning sideways due to drowsiness
- Immediate audio alert using a `.wav` beep sound
- Uses pretrained facial landmark model from Dlib

***

## Technologies Used

- Python 3.x
- OpenCV
- Dlib
- shape_predictor_68_face_landmarks.dat (Dlib’s facial landmark model)
- Pygame / Playsound (for audio alert)
  
***

## Project Structure

```
Driver-Drowsiness-Detection/
│
├── drowsiness_detection.py         # Main script for drowsiness detection
├── shape_predictor_68_face_landmarks.dat   # Facial landmarks pretrained model
├── music.wav                       # Beep audio alert file
├── README.md                       # Project documentation
├── requirements.txt                # Python dependencies list
```

***

## Installation & Setup

1. **Clone the repository**  
```bash
git clone https://github.com/your-username/driver-drowsiness-detection.git
cd driver-drowsiness-detection
```

2. **Create a virtual environment (recommended)**  
```bash
python -m venv venv
source venv/bin/activate      # On Windows use `venv\Scripts\activate`
```

3. **Install dependencies**  
```bash
pip install -r requirements.txt
```

4. **If not included, download the facial landmark model file**  
Download `shape_predictor_68_face_landmarks.dat` from the official Dlib model source and place it in the project folder.

***

## Usage

Run the drowsiness detection system with the command:

```bash
python drowsiness_detection.py
```

- The system will start your webcam and begin monitoring your face in real time.
- It calculates the Eye Aspect Ratio (EAR) to check if your eyes close beyond a threshold for a sustained time.
- It also detects if your head tilts sideways indicating drowsiness.
- On detecting drowsiness, the system plays a beep alert from `alert.wav` to wake you up.

***

## How It Works

- Captures live video from your webcam.
- Uses Dlib to detect facial landmarks and identify eye and head positions.
- Calculates EAR to quantify how open your eyes are.
- Monitors head position for tilt or lean.
- When drowsiness signs are detected, triggers an audio beep alert.

***

## Dependencies (requirements.txt example)

```
opencv-python
dlib
numpy
pygame
```

***

## Future Enhancements

- Add yawning detection using mouth aspect ratio.
- Integrate with vehicle systems for broader safety alerts.
- Use deep learning models for improved accuracy.
- Mobile and embedded system compatibility.

***

## License

This project is for educational and research purposes. Feel free to modify and use it with appropriate credit.
[9](https://www.youtube.com/watch?v=SIZNf_Ydplg)
[10](https://hda10196.h-da.io/face-image-quality-toolkit/source/readme.html)
