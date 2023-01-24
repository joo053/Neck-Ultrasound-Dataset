# Neck-Ultrasound-Dataset
NNUS: Large Dataset for Normal Neck Organ Detection in Ultrasound 

**Summary statement**
Ultrasound images of the neck are often noisy and artifacts, requiring extensive experience to accurately identify the human organ. Therefore, image detection models trained on a large dataset for Normal Neck Ultrasound (NNUS) images have the potential to help doctors and radiologic technologists in real time. It can also be used for educational purposes for students learning radiology and can be usefully used to distinguish it from normal people by adding an abnormal dataset.
The anatomical appearance of the normal person's neck and ultrasound images of the organs and its label dataset can shorten the time for many researchers to photograph and collect the normal person's neck for their research after publication. In addition, many researchers can develop new models using their datasets and extra-validate their studies using these datasets.

**Abstract**
-	Our NNUS dataset consists of 790 normal human sonography images and their labels.
- We trained 100 epochs using YOLOv5s pretrained model and obtained mAP 0.8044, precision 0.7952, recall 0.8082.
- For the validation of the model we have learned, we input the newly captured normal person's neck ultrasound, and we were able to obtain the detected video as shown below.

## Table of Contents
- [Structure of Dataset](#structure-of-dataset)
- [Usage](#usage)
- [Results of Training](#results-of-training)
- [Acknowledgements](#acknowledgements)

## Structure of Dataset
        NNUS/
        ├── images
        │   ├── 0001.jpg       <- Ultrasound images
        │   ├── 0002.jpg
        │   └── 0003.jpg
        └── labels
            ├── 0001.txt       <- Label 
            ├── 0002.txt
            ├── 0003.txt
            └── classes.txt    <- Class
### Images
All images are composed of 494×447 pixel jpg format files.
All shots were taken from 25 volunteers (average age 24.5 ± 3.5 years), presumed to be disease-free, ultrasound images of the neck.
More than 3 Shingu College (Seongnam, Republic of Korea) sonography students participated in the scan.
This dataset is the result of scanning and extracting images using LOGIQ P6 (GE healthcare, Connecticut, U.S.). Three types of scanning methods (longitudinal, transverse, and oblique scan) were randomly applied, and scanned about 30 to 40 images per person.


### Labels
Two radiologic technologists (11 years and 6 years of experience) used Label-Img (Tzutalin. LabelImg. Git code (2015). https://github.com/tzutalin/labelImg) to label the trachea, thyroid, common carotid artery, internal jugular vein, esophagus, longus colli muscle, strap muscle, and sternocleidomastoid muscle with bounding boxes.
The location information of these boxes was converted into coordinates and saved as a text file.

<img src="table1.png" width="768px" />

## Usage
<img src="figure1.png" />

1. 
For more information about [nnU-Net](https://github.com/MIC-DKFZ/nnUNet), please read the following paper:


    Isensee, F., Jaeger, P. F., Kohl, S. A., Petersen, J., & Maier-Hein, K. H. (2020). nnU-Net: a self-configuring method 
    for deep learning-based biomedical image segmentation. Nature Methods, 1-9.
    

6. Download the model `best.model` file through the following [download](https://drive.google.com/file/d/1w7N0z901rAzuC6I7AarVbNE7c5DZyQjk/view), and move it to `BM_detection_AI/results/nnUNet/3d_fullres/meta/nnUNetTrainer__nnUNetPlans/all`.

## Acknowledgements
This code borrows from
- [MIC-DKFZ/nnUNet](https://github.com/MIC-DKFZ/nnUNet)
