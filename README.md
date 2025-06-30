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
 - Duplicate or missing image IDs in annotations

5. **Category/Class Distribution**  
 Analyzed how frequently each object category appears.

6. **Filtered for 10 Relevant Classes**  
 Only retained annotations for the selected 10 object classes.

7. **Visualizations**
 - Bar charts for class frequency
 - Sample image with overlaid bounding boxes

8. **Anomaly Detection**
   To get the number of missed datas
---

## Data Preprocessing

- Converted BDD100K's **JSON annotations** to **YOLOv8-compatible `.txt` format** (1 text file per image).

## Model Training

- Framework: **Ultralytics YOLOv8**
- Strategy:
- Performed **incremental training** by splitting the dataset into batches of 100 images.
- Each batch was trained for 5 epochs.
- The best model from each batch was used to initialize the next batch training.
- Final model is trained on ~69,863 images across batches.

## Sample Visualization

*(Add your actual charts/screenshots here)*

- Class distribution chart  
- Annotated image samples  
- Anomaly examples (missing boxes, duplicates)

---

## Project Status

- [x] Data analysis completed  
- [x] 10 classes selected  
- [x] JSON to YOLO format converted  
- [x] YOLOv8 training completed (batch-wise)  
- [ ] Evaluation & Inference *(in progress)*
---

## Feedback
Feel free to add comments
