# Fingertip Detection Project Overview

## Course Details
- **Course Number:** CSE 666
- **Assignment:** Programming Assignment 2
- **Professor:** Nalini Ratha

## Team Information
- **Student:** Ronak Haresh Chhatbar
- **UBName:** ronakhar
- **Teammates:** Ronak Haresh Chhatbar

## Project Goal
The objective of this project is to segment and detect fingerprint regions from a series of hand selfie images using advanced image processing and machine learning techniques.

## Project Description
This project involves several stages of development, from initial data collection to final testing of the detection algorithm. It encapsulates the following tasks:

1. **Data Collection:** A personal dataset of hand images is curated with different orientations and distances.
2. **Annotation:** Hand images are annotated to highlight visible fingerprint regions.
3. **Detection:** A YOLOv4-tiny object detection model is trained using Darknet to identify fingerprint regions within the images.
4. **Validation:** The developed algorithm is validated against annotated images to gauge its performance.
5. **Testing:** The algorithm is tested with an unseen dataset to evaluate its effectiveness in real-world scenarios.
6. **Reporting:** A detailed report is drafted to discuss the algorithm's design, methodology, and performance outcomes.

## Model Development and Results
- The detection algorithm is based on the YOLOv4-tiny model, which offers a balance between speed and accuracy.
- The model was trained on an augmented dataset that includes a variety of hand images to ensure diversity in the training process.
- The performance of the model was rigorously evaluated, showing promising results:
  - Precision and recall rates were calculated to understand the model's accuracy.
  - The mean Average Precision (mAP) achieved was 76.71% for the validation set and 100% for the testing set.
- The results indicate that the model can accurately detect fingertips with a high confidence level in diverse image conditions.

## Future Scope
The potential improvements to the project include:
- Expanding the dataset significantly to improve the model's robustness.
- Utilizing a more complex network structure like full YOLOv4 for potentially better accuracy.
- Optimizing the model further to run efficiently on specific hardware platforms, which may aid in real-time applications.

## References
This project references several open-source tools and libraries which are instrumental for object detection and image processing tasks. The detailed list of references can be found within the project documentation.

## Conclusion
The project demonstrates a successful approach to detecting fingertip regions in hand selfie images. The developed model shows high accuracy in both controlled and uncontrolled environments, which paves the way for future applications in biometric identification systems.

---

*Note: This README is intended to provide an overview of the project's scope, methodologies, and outcomes. It does not include instructions for setting up the environment or executing the code.*
