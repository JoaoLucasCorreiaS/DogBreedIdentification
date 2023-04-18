# Identifying a breed of a dog
In this notebook there's code that makes us able to identify a dog breed from a simple photo.

## 1. Problem
Identifying a dog breed given an image of a dog.

## 2. Data
The data I'm using is from Kaggle's dog breed identification competition.

## 3. Evaluation
The evaluation is a file with prediction probabilities for each dog breed of each test image.

## 4. Features
Some information about the data:

I'm dealing with images (unstructured data), so it's probably best we use deep learning/transfer learning.
* There are 120 breeds of dogs (120 different classes).
* There are about 10,000 images in the training set (these images have labels).
* There are about 10,000 images in the test set (these images have no labels because we'll want to predict them).

## 5. Code and resourses used
**Python version:** 3.11

**Packages:** TensorFlow, Pandas, IPython, OS, NumPy, Matplotlib and Keras.

## 6. EDA and getting the data ready
* Getting an idea of how many images I have
![image](https://user-images.githubusercontent.com/106838561/232871993-1bdb99cf-ecfe-4551-a768-e12a34631b07.png)
* Creating a list of pathnames from images ID's
* Creating the validation set
* Preprocessing the images turning them into tensors
* Finally turning the data into batches

## 7. The model
The model used was MobileNet V2, from TensorFlow Hub (https://tfhub.dev/google/imagenet/mobilenet_v2_130_224/classification/5)

## 8. Results
A pretty good accuracy was obtained. So I used the model to make predictions on my custom set of images. The result:
![image](https://user-images.githubusercontent.com/106838561/232875669-72252076-eda1-4c38-8e27-467dc50c3d4c.png)
