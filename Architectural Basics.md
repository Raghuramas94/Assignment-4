How many layers- We must start the network with an intuition about how many layers we would need in the network
Kernels and how do we decide the number of kernels? - The number of kernels must be considered before starting off with the network
3x3 Convolutions,- The convolution operation must be performed next 
Receptive Field, - The receptive field must be determined next and we must draw an intuition about obtaining the ideal receptive field
Batch Normalization, - Batch normalization is performed in order to normalize the inputs 
Position of MaxPooling, - The position of the maxpooling operation must be determined so that we can apply the operation with reducing the channels inappropriately
MaxPooling,- Maxpooling is performed next so as to decrease the receptive field
1x1 Convolutions, - 1x1 Convolutions is applied next so that we can increase the number of channels as required 
SoftMax,- The results of the convolutions is sent to the softmax layer in order to produce a probability like number to get an intuition on the effectiveness of the operation
The distance of MaxPooling from Prediction, - we must determine this distance so that we can get a sense of how the network is performing
Concept of Transition Layers, - Transition layers must be introduced in accordance with the convolution layers
Position of Transition Layer, - The position of transition layers must be determined correctly, which varies the accuracy of the network
When to add validation checks - Validation checks must be added for every epoch so that the loss and validation accuracy are tracked for every epochs in conjunction with the training accuracy
Number of Epochs and when to increase them, - Based on the accuracy and the predictions, we can train the network on more number of epochs to imporve the accuracy 
The distance of Batch Normalization from Prediction, - This distance must be determined in order to change the position of BN and the number of times BN is performed
When do we introduce DropOut, or when do we know we have some overfitting - The concept of Dropout is introduced based on the performance of the network, in order to reduce overfitting and 
DropOut - Droupout is introduced at specific points in the network in order to reduce the difference between the training and test error 
How do we know our network is not going well, comparatively, very early - The network's performance is evaluated after the initial few epochs and if the network is found to be producing significantly lower accuracy than required,it is found to be not a good network
Image Normalization, - the input images are normalized so that the network is able to train on better pre processed images which results in better predictions
Batch Size, and effects of batch size - The batch size is varied according to the network's performance 
Learning Rate, - Learning rate is introduced to control the effect of backprop and let the network control how much it learns and what it learns 
LR schedule and concept behind it - This concept is introduced in order to make learning rate a parameter for the neural network to learn by itself to set the ideal learning rate
When do we stop convolutions and go ahead with a larger kernel or some other alternative (which we have not yet covered) - We do this when the network is found to be not leanring anything and giving a similar accuracy over several epochs
Adam vs SGD - This is considered for complex networks where the performance of one optimizer must provide a slightly different accuracy when compared to the other
