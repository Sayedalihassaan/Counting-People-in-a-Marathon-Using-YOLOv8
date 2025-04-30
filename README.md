## Counting People in a Marathon Using YOLOv8
This project implements a real-time people counting system for marathon videos using the YOLOv8 object detection model and a custom tracker. It detects and tracks individuals in a video, counting those who cross a predefined line, with results visualized on the video feed.

## Features

Object Detection: Uses YOLOv8 to detect people in video frames.
Tracking: Tracks individuals across frames with unique IDs using a custom Tracker class.
Counting Mechanism: Counts people crossing a horizontal line in the video.
Visualization: Displays bounding boxes, IDs, and a count of people on the video output.

## Requirements

Python 3.7+
Libraries:
ultralytics
opencv-python
numpy
pandas
cvzone


A YOLOv8 model file (e.g., yolov8s.pt)
A coco.txt file containing class names (included in the repository)

Install the required dependencies using:
pip install ultralytics opencv-python numpy pandas cvzone

Installation

Clone the repository:git clone https://github.com/your-username/counting-people-marathon-yolov8.git
cd counting-people-marathon-yolov8


Install the dependencies:pip install -r requirements.txt


Download a YOLOv8 model (e.g., yolov8s.pt) from the Ultralytics YOLOv8 repository and place it in the project directory.
Ensure the coco.txt file is present in the project directory (included in the repository).
Place your input video file (e.g., p3.mp4) in the project directory.

Usage

Prepare the Environment:

Ensure the YOLOv8 model (yolov8s.pt), coco.txt, and the input video (p3.mp4) are in the project directory.
The Tracker class (assumed to be in tracker.py) must be available in the project directory.


Run the Notebook:

Open the Counting people in a marathon using YOLOv8.ipynb notebook in Jupyter Notebook or JupyterLab:jupyter notebook "Counting people in a marathon using YOLOv8.ipynb"


Execute the cells sequentially to:
Load the model and video.
Detect and track people.
Count individuals crossing the line at y=383.
Display the output video with bounding boxes, IDs, and the count.




Output:

The video feed displays:
Bounding boxes around detected people with unique IDs.
A green line at y=383 for counting.
A red dot on people crossing the line.
A text box showing the total count of people (people count: <number>).


Press q to exit the video display.


Customization:

Adjust the counting line position by modifying cy1=383 in the code.
Change the offset value (default 4) to adjust the sensitivity of the counting zone.
Replace p3.mp4 with your video file.



Project Structure
counting-people-marathon-yolov8/
│
├── Counting people in a marathon using YOLOv8.ipynb  # Main Jupyter Notebook
├── tracker.py                                       # Custom Tracker class
├── coco.txt                                        # COCO class names
├── yolov8s.pt                                      # YOLOv8 model (to be downloaded)
├── p3.mp4                                          # Input video (to be provided)
├── requirements.txt                                # Required dependencies
└── README.md                                       # This file

Notes

The tracker.py file is not included in the provided document but is assumed to contain the Tracker class for object tracking. Ensure it is available or implement a compatible tracking solution.
The counting line (cy1=383) and offset (offset=4) are tuned for the provided video resolution (1020x500). Adjust these for different videos or resolutions.
The project uses the COCO dataset class names (coco.txt) to filter for the person class.

Contributing
Contributions are welcome! Please follow these steps:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Commit your changes (git commit -m "Add your feature").
Push to the branch (git push origin feature/your-feature).
Open a pull request.

License
This project is licensed under the MIT License. See the LICENSE file for details.
Acknowledgments

Ultralytics YOLOv8 for the YOLO implementation.
cvzone for visualization utilities.
The open-source community for providing invaluable tools and resources.

Contact
For questions or issues, please open an issue on GitHub or contact saiedhassaan2@gmail.com
