
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

Model1 -  2 Layer Conv-net with 1 Fully connected Layer
------
Batch size = 400, epoch = 300
Regularization: Dropout (0.25)

| Data Sets         | RMSE |
|-------------------|------|
| Training Set      | 1.92 |
| Dev Set           | 1.92 |
| Test Set (Kaggle) | 4.44 |
