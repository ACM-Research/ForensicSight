
To assist forensics experts in identifying what events took place at the scene of a crime, you will learn the basics of image classification and train a model using convolutional neural networks (CNNs) to classify bloodstain patterns commonly found in crime scenes into three categories: passive, transfer, and impact.

![LegalEye_Poster_-1](https://github.com/ACM-Research/ForensicSight/assets/73293294/d022d1a8-8e61-4a61-83da-a625d66c7ffb)


### Introduction
In the realm of forensic investigations, decoding the intricate details of crime scenes is essential for unraveling the mysteries surrounding criminal activities. A crucial element in the deciphering aspect of this investigation process involves identifying and interpreting the various bloodstain patterns across different surfaces, which can further provide valuable insights into the sequence of events that transpired.

In this research project, we mainly immerse ourselves in the fundamentals of image classification using advanced techniques such as convolution neural networks (CNNs). Our primary goal is to assist aspiring forensic analysts and machine learning enthusiasts with a sophisticated model. This model excels as classifying bloodstain patterns - a task of utmost significance in forensic science—into two distinct categories: passive, and transfer. 

### Methods
1. Research
    Before we started to create a model,  we employed online resources regarding YOLOv7, PyTorch, and OpenCV, and an open source algorithm. Furthermore, we expanded our knowledge via numerous previous research papers; however, we expanded our knowledge by adapting our model to different surfaces.
2. Creating the dataset
    We compiled blood stains across different surfaces dataset with over 300 images in order to train our model.
3. Training the model
    With the dataset, we trained our model by using preprocessed images with bounding boxes identifying the classification of the stain. Then we further augmented our data using standard industry techniques like 3 types of rotations, vertical flips, and horizontal flips.
4. Testing the dataset
    Once the YOLOv7model was done training, we started our experiment. Our team repeated trials to gain accuracy in accuracy of stain detection across different surfaces until an accuracy score to satisfaction was received. 

### Computer Vision and Object Detection
Computer Vision, a subfield of AI focused on computers gaining an understanding of something from digital media, is the basis of ForensicSight.

We utilized YOLOV7, an open-source algorithm for real-time object detection, because it is tailored towards faster and more accurate results as opposed to other such algorithms or other algorithms within the YOLO architecture.

YOLOv7 assists ForensicSight in developing a model that can detect bloodstains across various surfaces. With the large amount of crimes that occur on a daily basis, it is pivotal that Forensics labs are quick and accurate in the information they provide from what they receive. 

### Results
To measure the accuracy of our model, we focused on an MAP score at two IOU scores. The higher the IOU readings, the more accurate our results and a higher MAP means a more accurate model. This is because the IOU score measures the overlap of the annotated and predicted bounding boxes over the combined space of the predicted bounding boxes. The MAP score measures the overall accuracy of the model in relation to precision and recall.

The data shows us that after 300 epochs of training, we end with a precision score of 0.8133, recall score of 0.6409, and MAP scores of 0.7027 at an IOU score of 0.50, and 0.4518 at an IOU score of 0.95

![Screenshot 2024-04-29 115011](https://github.com/ACM-Research/ForensicSight/assets/73293294/06fbbbda-972c-422a-88bb-bb19c2cfe3c9)


### Analysis
![analysisImage](https://github.com/ACM-Research/ForensicSight/assets/73293294/e55c69f0-f5f6-49ab-ae78-05775a1f4914)

As demonstrated by the graphs, ForensicSight has a high MAP score of 0.7027 demonstrating that it can correctly detect passive and transfer stains 70.27 \% of the time with respect to our dataset. The data also shows a high precision score of 81\% showcasing that 81\% of the time the model predicts the right bloodstain with respect to the class. A recall of 64\% suggests that the model is able to find a class of the total number of that class present 64\% of the time.

Our Confusion Matrix above also highlights some areas where large discrepancies are occurring in the detection part of our model. Specifically, the darker boxes in the Transfer True Column and Background FN Predicted Row indicate that in 52\% of transfer images, there is no stain being detected. Passive stains on the other hand do a great job of being detected by our model as 83\% of classified passive stains from our dataset were detected by our model.

### Conclusions
With further feedback and improvement changes, our machine learning model for blood stain detection can serve as a crucial element in deciphering the mysteries of criminal activities at a more efficient pace. With the main objective of making the detection of blood stains easier, our model can also help with providing a potential layout of the events that took place. This could greatly help forensic analysts who utilize our model for real-time and real-life accurate detection of blood stains. 

### Team Members
Abis Naqvi
Zara Iqbal
Sriram Sendhil
Amulya Rayabhagi
Aarushi Gupta
Nivedha Sreenivasan (Project Lead)
Dr. Dohyeong Kim (Faculty Lead)
