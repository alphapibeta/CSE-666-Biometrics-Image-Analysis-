# CSE666 Programming Assignment 1
### Professor - Nalini Ratha
### UBName - ronakhar; Person # - 50477951
### Teammates - Ronak Haresh Chhatbar

## Task 1: Annotation
- Mark bounding boxes for each face in the image and save them using any tool.
- Utilized LabelMe for annotation, labeling 129 images.

## Task 2: Face Detection
- Utilize the `face-image-analysis` repository and the MTCNN model for face detection.
- `congress.jpg` resulted in 133 detected faces with the best threshold of 0.98.
- `get_bounding_box` function retrieves bounding boxes in x1, x2, y1, y2 format.
- `get_iou` function evaluates the Intersection over Union (IoU) for the bounding boxes against the ground truth with varying thresholds.

**Result Evaluation:**
- IOU threshold at 0.4 and 0.8 yields 126 bounding boxes indicating good detection accuracy.

## Task 3: Sentiment/Expression Analysis
- Employ `face-emotion-recognition` library with `mobile_net7` model for expression analysis.
- `get_emotions` function processes each ROI and classifies into one of seven emotions.
- Predictions saved in an "emotions" folder, with the naming format `<file_number_emotion>.png`.
- Without ground truth, manual evaluation suggests the prevalence of "Anger" in the predictions.

## Task 4: Gender Classification
- Use `face_classification` repository and `simple_CNN.81-0.96.hdf5` TensorFlow model.
- `get_gender` function slices the image based on bounding boxes to identify gender.
- Adjustments made to include forehead and head-hair features improve accuracy.
- Classified 24 as women and 109 as men, with precision and recall metrics calculated for each gender.

**Evaluation Metrics:**
- Precision for Women: 0.41
- Recall for Women: 0.41
- F1 Score for Women: 0.41
- Precision for Men: 0.84
- Recall for Men: 0.88
- F1 Score for Men: 0.86
- Combined F1 Score: 0.79

## Task 5: Face Pose Estimation
- Utilize `Rotation Representation for Unconstrained Head Pose Estimation` library.
- `get_headpose` function estimates the pitch, yaw, and roll of each face.
- Classification of head tilt is based on yaw value.
- Output saved in "headpose" folder, with the naming convention indicating the direction of the tilt.

## Task 6: Feature Extraction
- Implement `ARC-face` model for feature extraction.
- `generate_embds` function processes each face to produce (1, 512) embeddings.
- `save_embeddings` function stores embeddings for all 133 faces.

## Task 7: Face Recognition
- `make_comparassion` function identifies each ROI against a dataset of lawmakers.
- Encodings from the dataset and the generated embeddings from Task 6 are compared using Euclidean distance.
- Correctly identified faces are labeled with the Senator/Congressperson's name or "Unknown" for non-lawmakers.

**References:**

### Task 1:
- [LabelMe Annotation Tool](https://github.com/wkentaro/labelme)

### Task 2:
- [MTCNN Face Detection](https://github.com/ipazc/mtcnn)

### Task 3:
- [Face Emotion Recognition Library](https://github.com/HSE-asavchenko/face-emotion-recognition)
- Model: `mobilenet_7.h5`

### Task 4:
- [Face Classification GitHub Repository](https://github.com/oarriaga/face_classification)

### Task 5:
- [Head Pose Estimation Library](https://github.com/yinguobing/head-pose-estimation)

### Task 6:
- [ARC-face Model for Feature Extraction](https://github.com/deepinsight/insightface)

### Task 7:
- Comparison and Recognition based on embeddings from ARC-face.

