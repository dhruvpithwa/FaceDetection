

Problem Statement: To detect faces from dataset and crop the faces detected and save it in another folder with extension jpg.

Approach: 

There are two methods implemented in this project to detect faces.

Method 1: 

	Using Haar-Cascade

	Haar Cascade is a machine learning-based approach where a lot of positive and negative images are used to train the classifier.

	Positive images – These images contain the images which we want our classifier to identify.
	Negative Images – Images of everything else, which do not contain the object we want to detect.


	The output of this method is stored in folder Output-HAARCASCADE.


Method 2:
	
	Using Multi-task Cascaded Convolutional Neural Network 
	
	MTCNN is an algorithm consisting of 3 stages, which detects the bounding boxes of faces in an image along with their 5 Point Face Landmarks.
	
	Each stage gradually improves the detection results by passing it’s inputs through a CNN, which returns candidate bounding boxes with their 
	scores, followed by non max suppression.
	
	In stage 1 the input image is scaled down multiple times to build an image pyramid and each scaled version of the image is passed through it’s CNN.
	
	In stage 2 and 3 we extract image patches for each bounding box and resize them (24x24 in stage 2 and 48x48 in stage 3) and forward them through the CNN of that stage.
	
	Besides bounding boxes and scores, stage 3 additionally computes 5 face landmarks points for each bounding box.

	The output of this method is stored in folder Output-MTCNN.
