# CelebA-Face Detection

## Task description
Given your task (Semantic Segmentation or Object Detection), you have to test three (3) pretrained models on the test set of a given dataset, comparing the results between the models. For the comparison, you have to use at least three (3) metrics commonly used in your task.

For example, if student A is given Object Detection task and the Ballons v2 dataset, then his/her task is to choose 3 pretrained object detection models [R-CNN, YOLO, ...] and evaluate them on the Ballons v2 test set, comparing the results using 3 metrics [mAP, Recall, ...]. If a dataset does not have a testing set, then the student should split at least 10% of the training set to create the test set.

For running test/evaluation/inference on a pre-trained model, it is important to know what are the model requirements, so that the input is preprocessed accordingly. Make sure to explore the data and present detailed evaluation metrics.

## Conclusion
First loaded the data from kaggle( the real one not the one with wrong annotations). Since Data is big we used only one part and I defined num_samples variable that helps us control the size of the test test. Each part of the data consists of 10 000 samples and the deafult for us was 2000 ( It is low because of the long runtime of some models). After preprocessing and displaying the images we loaded the models. First we predicted only one image and then the whole testset. After creating boxes variables we checked them with 4 metrics ( IOU, Precision, Recall and F1 Score). All the models I have used had one common problem they returned bigger area than the real box which was leading higher precision but lower recall. One more thing to add is that the real boxes which are given are sometimes not accurate too. It is really hard to define what really is face is and where it ends. Maybe some 3D approaches will give us more detailed results about face. But thats a work another day
