# Out of Space Detection - Real-Time Empty Shelf Detection

## Project Overview
This project, **Out of Space Detection**, focuses on detecting empty spaces in supermarket shelves in real time using computer vision. The system leverages a fine-tuned YOLOv8 model to automatically identify out-of-stock or empty shelf spots, helping retailers maintain inventory efficiently.

## Dataset
The dataset used contains 2,697 images of supermarket shelves, both empty and stocked. The dataset can be found at [Roboflow](https://universe.roboflow.com/aneesh-obmai/empty-space-brfvt). Key features of the dataset include:
- Multiple angles of shelf spaces.
- Diverse lighting conditions.
- Clearly marked empty shelf regions for model training.

## Model Architecture
- **Model**: YOLOv8s
- **Training**: The model was fine-tuned for 50 epochs on the dataset.
- **Optimization**: Standard YOLOv8 optimization techniques were applied, including early stopping and data augmentation.

### Performance Metrics
- **Mean Avarage Percesion (mAP)**: 0.87

## Real-Time Detection
The real-time detection is implemented using **OpenCV** to process live video feeds and detect empty shelf spaces. The model runs inference on each video frame, highlighting areas where stock is missing. This system could be deployed with surveillance cameras in supermarkets for real-time monitoring.

## How to Run

### Prerequisites
Ensure you have the following dependencies installed:
- Python 3.x
- YOLOv8 (Ultralytics)
- OpenCV
- Roboflow SDK (optional, if pulling the dataset programmatically)

Install dependencies:
```bash
pip install ultralytics opencv-python-headless
```
## Results
The model performs with a high level of accuracy, achieving an mAP of 0.87, successfully identifying empty shelves in real-world conditions.

## Future Work
Possible improvements include:
- Extending the model to detect low-stock levels, not just fully empty spaces.
- Optimizing real-time performance for deployment on edge devices (e.g., Raspberry Pi).
- Expanding the dataset with more challenging environments and variations.
