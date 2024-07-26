# Fall Detection System

This project uses a fall detection system that leverages YOLO (You Only Look Once) for object detection and OpenCV for video processing. When a fall is detected, an alert sound is played using the Pygame library.

## Features

- Detects falls in a video using YOLO object detection.
- Plays an alert sound when a fall is detected.
- Stops the sound when no fall is detected.

## Requirements

- Python 3.11.8
- OpenCV
- YOLOv8 model
- Pygame
- Ultralyitcs YOLO (for model inference)

## Installation

1. **Clone the Repository**

    ```bash
    https://github.com/AmmarMohamed0/Fall-Detection-System.git
    cd Fall-Detection-System
    ```

2. **Install Dependencies**

    Install the required Python packages. It is recommended to use a virtual environment.

    ```bash
    pip install notebook opencv-python pygame ultralytics
    ```

3. **Download YOLOv8 Model**

    Ensure that the YOLOv8 model file (`yolov8s.pt`) is placed in the same directory as your script. 

4. **Prepare the Sound File**

    Place your alert sound file (`alert.mp3`) in the same directory as your script.

5. **Prepare the COCO Class Names**

    Ensure you have the `coco.txt` file with class names used for detection. This file should be in the same directory as your script.

## Usage

1. **Open the Notebook**

    Open the Jupyter notebook in your preferred environment. If you don’t have Jupyter installed, you can install it via pip:

    ```bash
    pip install notebook
    ```

2. **Start Jupyter Notebook**

    Launch Jupyter Notebook from the command line:

    ```bash
    jupyter notebook
    ```

    This will open the Jupyter interface in your web browser.

3. **Run the Notebook**

    Navigate to the `AlertFall.ipynb` file in the Jupyter interface and open it. Run the cells in the notebook to start the fall detection system.

    The notebook will display video processing results in the output cells. If a fall is detected, an alert sound will play.

4. **Stop the Notebook**

    To stop the execution of the notebook, interrupt the kernel by clicking the "Stop" button in the Jupyter interface or close the notebook.

2. **Exit the Application**

    To exit the application, press the 'q' key while the video window is in focus.

## Code Explanation

- **Video Capture**: The script captures video frames from the specified video file (`fall.mp4`).
- **Model Inference**: YOLOv8 is used to detect objects in each frame.
- **Fall Detection**: If a detected person has an aspect ratio exceeding a specified threshold, it is considered a fall.
- **Sound Alert**: When a fall is detected, the alert sound is played. The sound stops when no fall is detected.

## Troubleshooting

- **Missing Files**: Ensure that `fall.mp4`, `yolov8s.pt`, `alert.mp3`, and `coco.txt` are in the correct directory.
- **Dependencies**: Verify that all required Python packages are installed.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- [Ultralytics YOLO](https://github.com/ultralytics/yolov5) for the YOLOv8 model.
- [OpenCV](https://opencv.org/) for computer vision functionalities.
- [Pygame](https://www.pygame.org/) for sound playback.
