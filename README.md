# Mini_project Lane detection using Computer Vision

## Lane Detection using OpenCV2

This project implements lane detection in videos using OpenCV2 and best practices for image processing and computer vision. The pipeline detects lane lines on a road from a video feed, computes the lane curvature, estimates vehicle position relative to the lane center, and visually overlays the lane detection on the video.

## Features

	•	Lane detection using color filtering and edge detection
	•	Perspective transform to get a bird’s-eye view of the road
	•	Histogram-based lane identification
	•	Sliding window search for accurate lane detection
	•	Polynomial fitting for lane curvature
	•	Calculation of vehicle offset from the lane center

## Technologies Used

	•	Python 3
	•	OpenCV2 for image processing
	•	NumPy for mathematical operations
	•	Matplotlib for plotting
	•	Video Processing for lane detection 

## Setup Instructions

**1. Install Required Packages** : Ensure you have the following packages installed: pip install numpy opencv-python matplotlib

**2. Directory Setup** : Ensure the video file (drive.mp4) is placed in the working directory where the script is executed.

**3. Run the Script** : The script processes the video to detect lanes and output the lane overlay on each frame in real-time. Execute the script as: python lane_detection.py

## Key Functions

**readVideo()** : Reads the input video from the working directory.<be>

**processImage()** : Processes each frame of the video, applying HLS color filtering, grayscale conversion, thresholding, blurring, and edge detection to highlight lane lines.<be>

**perspectiveWarp()** : Applies a perspective transformation to give a bird’s-eye view of the road, making it easier to detect lanes.<be>

**plotHistogram()** : Plots a histogram of white pixels in the bottom half of the image, helping locate the base of lane lines.<br>

**slide_window_search()** : Uses a sliding window technique to search for lane lines and fits a second-degree polynomial to the detected lanes.

**general_search()** : Performs a lane search based on the previously detected lane polynomials for better stability over frames.

**measure_lane_curvature()** : Calculates the curvature of the lanes in meters and determines the direction of the curve (left, right, or straight).

**draw_lane_lines()** : Overlays the detected lane lines and lane area on the original image, visualizing the lane detection results.

**offCenter()**: Calculates the vehicle’s position relative to the center of the lane.

**addText()** : Adds informative text to the final output image, including the lane curvature and vehicle offset.

## Output

The output is the video with lane lines detected and a visual display of the lane curvature and vehicle’s deviation from the center.

**Best Practices Followed**

	•	Modular Code: Functions are broken down into smaller tasks for better readability and maintenance.
	•	Real-time Processing: The pipeline is optimized for real-time lane detection on video streams.
	•	Metric Conversion: The script uses meter-to-pixel conversion for accurate lane curvature and vehicle offset calculations.

**Potential Improvements**

	•	Lane Detection in Different Conditions: Add robustness to handle varying lighting and weather conditions (rain, fog).
	•	Multiple Lane Detection: Extend the functionality to detect multiple lanes and support multi-lane roads.
	•	Advanced Smoothing: Implement Kalman filtering or another technique to smooth lane detection results across frames.

**References**

	•	OpenCV documentation: https://docs.opencv.org/
	•	Lane detection algorithms: Research on computer vision and lane detection techniques.


