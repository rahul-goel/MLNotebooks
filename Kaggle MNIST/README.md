# Kaggle MNIST
The complete MNIST Dataset consisted of 60000 images which Kaggle divided into 42000 Train + 28000 Test.
I trained the models only on the 42000 training images and did not refer to the publicly available other images.

This is the first time I used PyTorch. Had a hard time figuring a lot of things out. But somehow managed to fit a Fully connected Network first.

## Fully Connected Network
Since the images are 28 x 28, it is within the computation power to unroll the entire images and train a FCN. I tried various architectures. But could not improve performance further. Got an accuracy of somewhat 93% in my submission to Kaggle.

## CNN
I coded the most basic CNN possible and used it. But I did a little something extra too. Data Augmentation. Look at the code -  Converted to PILImage and randomly rotated as well as shifted the image. And then trainined the CNN for several epochs. Ultimately the validation set accuracy was somewhat 95%.

Then I finalised the model, merged the training and the validation set to get a larger final set. And got a training accuracy of 94%. I tried variations but did not figure out why the accuracy decreased.

But when I submitted to kaggle I got an accuracy of 97% (in the bottom half since now people are achieving 100% accuracy). The main reason I think is Data Augmentation. Since the test data was "easier" to understand than the transformed data that I used for training and validation. Technically, I should have not transformed the validation set to keep the test set and validation set as close to each other as possible but I realised that after the submission.

Sometime later when I get fairly good at this stuff, I'll try to beat my current score.
