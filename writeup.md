# Traffic Sign Recognition

---

**Build a Traffic Sign Recognition Project**

The goals / steps of this project are the following:
* Load the data set (see below for links to the project data set)
* Explore, summarize and visualize the data set
* Design, train and test a model architecture
* Use the model to make predictions on new images
* Analyze the softmax probabilities of the new images
* Summarize the results with a written report

## Rubric Points
#### Here I will consider the [rubric points](https://review.udacity.com/#!/rubrics/481/view) individually and describe how I addressed each point in my implementation.  

---


#### 2. Include an exploratory visualization of the dataset.
which show  *histogram of label frequency*

##### Design and Test a Model Architecture

The images were converted into grey-scalte for better resultes and becaulse of time complexity as the depth of colored image is "3" and depth of grey image is "1".

you can also normalize the images as it is recomended to do so.

####2. Describe what your final model architecture looks like including model type, layers, layer sizes, connectivity, etc.) Consider including a diagram and/or table describing the final model.

My final model consisted of the following layers:

| Layer         		|     Description	        					| 
|:---------------------:|:---------------------------------------------:| 
| Input         		| 32x32x1 RGB image   							| 
| Convolution 3x3     	| 1x1 stride, same padding, outputs 28x28x6 	|
| RELU					| Activation functoin							|
| Max pooling	      	| 2x2 stride,  outputs 16x16x64 				|
| Convolution 3x3	    | 14x14x6	 									|
| Fully connected		| 84x43 i.e 3612        						|
| Softmax				|         										|
-------------------------------------------



#### 3.  how I trained your model.
* EPOCHS = 150
* BATCH_SIZE = 128
* Number of training set = 34799 
* Used 5 Lyers 
* drop used once in between layer was .5

#### 4. Approach taken for finding a solution and getting the validation set accuracy t
My final model results were:
* training set accuracy of 95.5
* validation set accuracy of 93.2
* test set accuracy of 1


* The best i could think of is to use greyscale i.e dimensioning imgage to (32,32,1) shape
* epoches were increased to 150 for better results
* drop was used
* one hot was quite a help for result finding 
*
