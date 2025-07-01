# Bosch_BDD_object_detection
This repo created based on object detection assignment given by BOSCH team

## Dataset
- Dataset used: **[BDD100K](https://bdd-data.berkeley.edu/)**
- Format: BDD100K comes with images and annotation files in **JSON format**.
- Focused object classes (10 total):
  ['bike', 'bus', 'car', 'motor', 'person', 'rider', 'traffic light', 'traffic sign', 'train', 'truck']
  
## Data Analysis Workflow

Before model training, we performed a detailed data inspection and visualization.

### Steps Included:

1. **Check File Existence**  
 Verified availability of all image and annotation files.

2. **Load Annotation Files**  
 Loaded json files from label folder

3. **Count Annotated Data**  
 Extracted and counted all annotated image,label pairs.

4. **Missing Data & Uniqueness Check**  
 Checked for:
 - Missing labels
 - Empty or corrupted entries
 
5. **Category/Class Distribution**  
 Analyzed how frequently each object category appears.

- Class distribution chart  
  ![image](https://github.com/user-attachments/assets/0be45578-e835-45b0-87a8-f78b1571fc78)

7. **Filtered for 10 Relevant Classes**  
 Only retained annotations for the selected 10 object classes.

8. **Visualizations**
 - Bar charts for class frequency
 - Sample image with overlaid bounding boxes

8. **Anomaly Detection**
   To get the number of missed datas
---

## Data Preprocessing

- Converted BDD100K's **JSON annotations** to **YOLOv8-compatible `.txt` format** (1 text file per image).

## Model Training

- Framework: **Ultralytics YOLOv8**
- 1. Without using pretrained weight file-Consider all dataset
- 2. Using pretrained weight and
- Perform **incremental training** by splitting the dataset into batches of 100 images.
- Each train for 5 epochs.

## Project Status

- [x] Data analysis completed  
- [x] 10 classes selected  
- [x] JSON to YOLO format converted  
- [x] YOLOv8 training Not completed (batch-wise)  

## Feedback
You're welcome to share any comments or suggestions.
