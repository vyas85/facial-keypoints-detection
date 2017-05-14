
Facial Keypoints Detection
======

-Goal: Predict locations of facial keypoints on images using Convolutional Neural Nets

-Deep Learning Framework: Tensorflow

Models trained 
------
-2 Layer Conv-Net with 1 Fully Connected Layer
-4 Layer Conv-Net with 1 Fully Connected Layer
-2 Layer Conv-Net with 2 Fully Connected Layers

Data Cleaning and Augmentation Techniques USed
------
-Dropping Training & Test cases with ‘NA’ values
-Flipping Images horizontally
-Applying Histogram Normalization

Other Augmentation Techniques Tried
------
-Moving Images 

Model 1 -  2 Layer Conv-net with 1 Fully connected Layer
------
Batch size = 400, epoch = 300
Regularization: Dropout (0.25)

| Data Sets         | RMSE |
|-------------------|------|
| Training Set      | 1.92 |
| Dev Set           | 1.92 |
| Test Set (Kaggle) | 4.44 |

-Without regularization, this model over-fit the data. 
-Adding dropout  prevented overfitting
-The model’s error was due to bias. The try to reduce this error, we tried to build more complex neural nets

Model 2 -  4 Layer Conv-net with 1 Fully connected Layer
------

Model3 -  2 Layer Conv-net with 2 Fully connected Layers
------
Batch size = 400, epoch = 400
Regularization: Dropout (0.2)

Conclusion
------
-Dropout is an effective technique for preventing overfitting. Models without dropout overfit significantly.

-Complex models by themselves are not sufficient to increase variance. Increasing the size of the training dataset is important to increase variance of the classifier

-It is important to choose the correct learning rate for the optimizer. Low learning rates mean that the optimizer takes a long time to train. High learning rates mean that  the model does not converge to a good minima

-Choosing the right batch size is important for stochastic gradient descent. Large batch sizes use significantly more memory but yield stable gradients. Small batch sizes are memory effective but yield noisy gradients

Future Work
------
-Try to use all the available training data by potentially fitting 2 neural nets - one for the 4 keypoints present in all the training data, and one the remaining keypoints
-Try additional data augmentation techniques to increase the size of the training data. eg. Rotations


