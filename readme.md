# **Object Tracking Using OpenCV with CSRT Tracker**

## **Project Overview**
This project demonstrates object tracking using OpenCV's CSRT (Discriminative Correlation Filter with Channel and Spatial Reliability) Tracker. The implementation supports both real-time webcam tracking and pre-recorded video file inputs. The tracking results are saved as an output video file.

---

## **Features**
- **Object Tracking**: Tracks a selected region of interest (ROI) in real-time or in video input.
- **Output Video Saving**: Saves the tracking output to a video file.
- **Time Limit for Webcam**: Limits the duration of webcam tracking to a specified number of seconds.
- **Resizable Input**: Allows resizing of input frames to optimize performance.

---

## **Folder Structure**
```
OpenCV/
├── images/                  # Store any example images (optional)
├── videos/                  # Store input videos
├── output.avi               # Generated output video (example)
├── Operations.ipynb         # Jupyter Notebook with code implementation
├── README.md                # Project documentation
└── .gitignore               # Ignore unnecessary files/folders like virtual environment
```

---

## **Requirements**
- Python 3.10.12
- OpenCV
- ipywidgets
- Jupyter Notebook

Install the dependencies using:
```bash
pip install opencv-python opencv-contrib-python ipywidgets matplotlib
```

---

## **How to Run**

### **1. Clone the Repository**
```bash
git clone https://github.com/BaratovSokhibjon/opencv.git
cd OpenCV
```

### **2. Run the Jupyter Notebook**
1. Open the `Operations.ipynb` file in Jupyter Notebook.
2. Run each code cell step-by-step.

### **3. Select Input Source**
- **Webcam Input**:
  Run the function with webcam as input:
  ```python
  track_and_save(0, scale_factor=0.5, output_path='webcam_output.avi', time_limit=10)
  ```
  This will start tracking through your default webcam for 10 seconds.

- **Video File Input**:
  Run the function with a video file:
  ```python
  track_and_save('videos/sample_video.mp4', scale_factor=0.8, output_path='video_output.avi')
  ```
  This will process the video file without any time limit.

---

## **How It Works**
1. **Region of Interest (ROI) Selection**:
   - The program allows you to select a region in the first frame of the video or webcam feed.
2. **Object Tracking**:
   - The CSRT Tracker tracks the selected ROI across frames.
3. **Output Video**:
   - The tracking result is saved to an output video file in `.avi` format.

---

## **Customization**
- **Time Limit**:
  Modify the `time_limit` parameter to change the duration of webcam tracking.
  ```python
  track_and_save(0, scale_factor=0.5, output_path='webcam_output.avi', time_limit=15)
  ```

- **Scaling Frames**:
  Adjust the `scale_factor` to optimize performance:
  ```python
  track_and_save('videos/sample_video.mp4', scale_factor=0.7, output_path='video_output.avi')
  ```

---

## **Output Example**
- The output video (`output.avi`) will contain the selected region tracked across frames with a bounding box.

---

## **Contributors**
- [Baratov Sokhibjon](https://github.com/BaratovSokhibjon)

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Let me know if you'd like further customization or additional sections for the README!