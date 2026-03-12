 # Automatic Detection and Summarization of Goal Events in Football Videos Using Deep Learning

## Overview
This project presents an automated system for detecting and summarizing key events in football match videos using deep learning and computer vision techniques. The system identifies important events such as **goals and missed shots** by analyzing football movement in video frames and automatically generates highlight clips from long match videos.

The system uses the **YOLOv8 object detection model** to detect the football in each frame and track its movement over time. By analyzing ball trajectory, velocity, and spatial location relative to the goal area, the system identifies shot attempts and classifies them as **goal or miss events**.

---

## Key Features
- Automatic football detection using **YOLOv8**
- Ball tracking across consecutive frames
- Motion and velocity analysis for shot detection
- Spatio-temporal event classification
- Automatic extraction of goal and miss highlight clips
- Efficient processing suitable for long match videos


---

## Methodology

The proposed system follows a structured pipeline:

### 1. Video Preprocessing
- Load football match videos
- Extract frames from the video
- Resize frames to a standard resolution
- Normalize frames for object detection

### 2. Ball Detection
- Use **YOLOv8 deep learning model** to detect the football in each frame.
- The model predicts bounding boxes and identifies ball positions.

### 3. Ball Tracking and Motion Analysis
- Track detected ball positions across consecutive frames.
- Calculate ball velocity using Euclidean distance.
- Analyze motion patterns to detect potential shot attempts.

### 4. Shot Detection
A shot event is detected when:
- Ball velocity exceeds a predefined threshold.
- The ball is located within a predefined **danger zone near the goal area**.

### 5. Goal and Miss Classification
After detecting a shot:
- The system observes ball trajectory for a short temporal window.
- If the ball enters the goal region → **Goal**
- If the ball does not enter the goal region → **Miss**

### 6. Highlight Extraction
- Extract corresponding video segments for detected events.
- Generate short highlight clips containing **goal and miss events**.

---

## Technologies Used
- Python
- YOLOv8 (Ultralytics)
- OpenCV
- NumPy
- Matplotlib
- Deep Learning
- Computer Vision

---

## System Architecture
The system pipeline consists of:

Video Input  
→ Frame Extraction  
→ YOLOv8 Ball Detection  
→ Ball Tracking  
→ Motion Analysis  
→ Shot Detection  
→ Goal/Miss Classification  
→ Highlight Clip Generation

---

## Dataset
The system is evaluated using **real football match videos** obtained from publicly available broadcast footage. The dataset includes long-duration videos with different camera angles, lighting conditions, and motion scenarios. :contentReference[oaicite:1]{index=1}

---

## Results
Experimental evaluation shows strong performance in detecting football events across different match videos.

Performance metrics include:
- Precision: up to **0.86**
- Recall: up to **0.84**
- F1-Score: up to **0.85**
- Accuracy: up to **0.84**

The system successfully reduces long football match videos into short highlight clips containing only key events. :contentReference[oaicite:2]{index=2}

---

## Performance
The system was tested on:

GPU: NVIDIA RTX 3060 (12GB)  
CPU: Intel i7 Processor  

Performance:
- **40–55 FPS processing speed**
- Efficient real-time event detection and video summarization. :contentReference[oaicite:3]{index=3}

---

## Applications
- Automated sports highlight generation
- Football video analysis
- Sports analytics platforms
- Broadcast video summarization
- Video content indexing

---

## Future Improvements
- Player detection and tracking
- Multimodal analysis using audio commentary
- Integration with transformer-based video models
- Real-time live match summarization

---
