# ForensicSight: Precise Crime Scene Bloodstain Classification
## Introduction
    In the realm of forensic investigations, decoding the intricate details of crime scenes is essential for unravelling the mysteries surrounding criminal activities. A crucial element in the deciphering aspect of this investigation process involves identifying and interpreting the various bloodstain patterns across different surfaces, which can further provide valuable insights into the sequence of events that transpired. 

    In this research project, we mainly immerse ourselves in the fundamentals of image classification using advanced techniques such as convolution neural networks (CNNs). Our primary goal is to assist aspiring forensic analysts and machine learning enthusiasts with a sophisticated model. This model excels as classifying bloodstain patterns - a task of utmost significance in forensic science—into two distinct categories: passive, and transfer. 

## Methods
  ## 1. Research
    Before we started to create a model,  we employed online resources regarding YOLOv7, PyTorch, and OpenCV, and an open source algorithm. Furthermore, we expanded our knowledge via numerous previous research papers; however, we expanded our knowledge by adapting our model to different surfaces. 

  ## 2. Creating the dataset
    We compiled blood stains across different surfaces dataset with over 300 images in order to train our model. 

  ## 3. Training the model
    With the dataset, we trained our model by using preprocessed images with bounding boxes identifying the classification of the stain. Then we further augmented our data using standard industry techniques like 3 types of rotations, vertical flips, and horizontal flips. 

  ## 4. Testing the dataset
    Once the YOLOv7model was done training, we started our experiment. Our team repeated trials to gain accuracy in accuracy of stain detection across different surfaces until an accuracy score to satisfaction was received. 

## Implementations
     We trained a dataset imported from Roboflow onto our model with around 300 epochs worth of iterations. Utilizing our data set, which was, different types of blood stains across different surfaces this machine model can be used in real life to help forensic analysts to do the same in real-time scenarios. In our simulated neural network environment, our dataset recognized the blood stains and began to classify and detect the multiple blood stains across different surfaces.

## Computer Vision and Object Detection
  Computer Vision, a subfield of AI focused on computers gaining an understanding of something from digital media, is the basis of ForensicSight.

  We utilized YOLOV7, an open-source algorithm for real-time object detection, because it is tailored towards faster and more accurate results as opposed to other such algorithms or other algorithms within the YOLO architecture.

  YOLOv7 assists ForensicSight in developing a model that can detect bloodstains across various surfaces. With the large amount of crimes that occur on a daily basis, it is pivotal that Forensics labs are quick and accurate in the information they provide from what they receive. 

## Results
    To measure the accuracy of our model, we focused on an MAP score at two IOU scores. The higher the IOU readings, the more accurate our results and a higher MAP means a more accurate model. This is because the IOU score measures the overlap of the annotated and predicted bounding boxes over the combined space of the predicted bounding boxes. The MAP score measures the overall accuracy of the model in relation to precision and recall.

    The data shows us that after 300 epochs of training, we end with a precision score of 0.8133, recall score of 0.6409, and MAP scores of 0.7027 at an IOU score of 0.50, and 0.4518 at an IOU score of 0.95
