# CIFAR - 10
My attempt at fitting the CIFAR - 10 dataset available at https://www.cs.toronto.edu/~kriz/cifar.html
After several attempts at tuning the architecture and the dropout parameters, I finally achieved some decent training accuracy of 89.75% and validation accuracy of 85.38%.
Upon testing on the official test set, the model an accuracy of 91.03%. The increase is because of Data Augmentation.
The data augmentation methods used were random horizontal flips and random rotations upto a certain limit.

However, the full training set wasn't used till now. After clubbing the training and validation sets to attain the original training set and training the same model with the same process on it, the training accuracy got upto 91.046.

With that the test accuracy I got was 93.168%. Decent I guess.
One thing I noted was the the model always slightly overfits. Despite of trying out several probabilities for dropout regularization, the model always had better training accuracy than validation accuracy by 4%-5%. But since the data was augmented before training, the test accuracy turns out to be better than the training accuracy.