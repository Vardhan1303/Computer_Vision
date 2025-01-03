# Task 1: Augmented Reality Using ArUco Markers

## Overview
This project implements augmented reality (AR) by overlaying poster images onto real-world scenes using ArUco markers. Using the OpenCV library, the program detects markers, calculates transformation matrices, and seamlessly integrates posters into captured images.

## Authors
- **Vardhan Vinodbhai Mistry**  & **Vaibhav Badgujar** 
- **Guided by:** Prof. Dr. Stefan Elser  

## Key Steps
1. **Aruco Marker Detection**  
   - Used OpenCV's `cv2.aruco.detectMarkers()` to identify marker positions and IDs.

2. **Creating Poster Dimensions**  
   - Calculated dimensions of concentric quadrilaterals to fit the poster on the detected marker.

3. **Warp Perspective Transformation**  
   - Used homography to align the poster with the marker's perspective.

4. **Merging Images**  
   - Integrated the poster with the classroom image using masking and blending techniques.

## Results
- Posters were successfully overlaid on 10 out of 11 images.  
- Minor alignment issues observed in 4 images due to perspective distortion.  
- Visual examples are provided in the `poster_overlayed/` folder.

## Repository Structure
- **`code/`**: Contains the Python scripts for marker detection, transformation, and merging.  
- **`report/`**: Includes the detailed file named details.md.  
- **`poster_overlayed/`**: Contains images demonstrating the project output.

## Acknowledgments

I would like to express my gratitude to the following resources and individuals for their invaluable support and guidance during this project:

- [OpenCV Documentation](https://docs.opencv.org/): For providing comprehensive documentation and examples that greatly assisted in developing the algorithms and code for this project.
- Prof. Dr. Stefan Elser: For providing the dataset and mentoring throughout the project.
