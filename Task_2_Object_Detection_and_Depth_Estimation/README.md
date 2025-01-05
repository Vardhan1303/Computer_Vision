## Task 2: Object Detection and Depth Estimation

This project demonstrates object detection using YOLOv8 and evaluates depth estimation for bounding boxes in a real-world scenario using the KITTI dataset. The task involves detecting objects, calculating distances to those objects, and comparing the estimated distances with the ground truth.

---

## Key Features
- **Object Detection**: Utilized YOLOv8 to detect objects in the KITTI dataset with high accuracy.
- **IoU Filtering**: Applied Intersection over Union (IoU) thresholds to refine YOLO bounding box results against ground truth data.
- **Depth Estimation**: Calculated real-world distances for detected objects using camera calibration parameters and bounding box information.
- **Data Visualization**: Annotated images with YOLO-detected and ground truth bounding boxes, including distance measurements.
- **Performance Analysis**: Created scatter plots to compare YOLO-estimated distances with ground truth distances for quantitative evaluation.

---

## Project Structure
```
|-- KITTI_Selection
|   |-- images               # Input images
|   |-- labels               # Ground truth bounding box and distance labels
|   |-- calib                # Calibration matrices for each image
|   |-- README.md            # Overview of the KITTI_Selection dataset
|-- bounding_box_coordinates # YOLO filtered bounding box coordinates and distances
|-- yolo_output              # Images with YOLO filtered bounding box
|-- results                  # Annotated images with bounding boxes and distances
|-- main.ipynb               # Main Jupyter notebook for processing
|-- Details.md               # Comprehensive explanation of the project
|-- README.md                # Overview of the project
```

---

## Prerequisites
1. **Python Packages**:
   Ensure the following libraries are installed:
   - `numpy`
   - `matplotlib`
   - `Pillow`
   - `ultralytics`

   Install dependencies with:
   ```bash
   pip install numpy matplotlib Pillow ultralytics
   ```

2. **Dataset**:
   - Download and organize KITTI dataset files in the `KITTI_Selection` directory as per the structure.

---

## Instructions

1. **Setup the Environment**:
   - Ensure all dependencies are installed and the dataset is correctly placed in the `KITTI_Selection` folder.

2. **Run the Jupyter Notebook**:
   - Open and execute `main.ipynb` step-by-step to process images, detect objects, and visualize results.

3. **Analyze Results**:
   - View annotated images in the `results` directory.
   - Examine scatter plots comparing YOLO-estimated distances with ground truth distances for performance evaluation.

## Results Summary:
   - Achieved an accuracy of 85% for detecting objects within a 5-meter range.
   - Observed minimal errors in depth estimation, primarily due to object overlaps and inaccuracies at greater distances.

## Future Enhancements
To further improve the system, the following steps can be undertaken:
- Expanding the dataset to include diverse scenarios, such as varying lighting and object occlusions.
- Refining calibration techniques to minimize distortion and enhance depth accuracy.
- Leveraging advanced object detection models to handle complex edge cases, including partial occlusions and dense object clusters.
---

## Acknowledgments
- [YOLOv8 Documentation](https://docs.ultralytics.com/): For guidance on implementing object detection.
- [KITTI Dataset](http://www.cvlibs.net/datasets/kitti/): For providing the dataset used in this project.
- [Camera Calibration and 3D Reconstruction - OpenCV Documentation](https://docs.opencv.org/4.x/d9/d0c/group__calib3d.html): For comprehensive insights on camera calibration and 3D reconstruction techniques.
- This project is part of the Master's program at the University of Applied Sciences Ravensburg-Weingarten, developed as an educational exercise.
- [OpenCV Documentation](https://docs.opencv.org/): For providing comprehensive documentation and examples that greatly assisted in developing the algorithms and code for this project.
---

## License
This project is licensed under the MIT License. See the LICENSE file for further details.
