# Data-Augmentation-with-CNN

In the application of image classification, one drawback may be the limited access to large data. In this study, we explored one possible solution to the limited amount of data, the data augmentation technique. Some previous studies have reported the effectiveness of traditional data augmentation techniques in improving the performance of image classifier. We used a less-used dataset named as Oxford-IIIT Pet dataset and artificially combined the images into two classes - dogs and cats. By training with three different Convolutional Neural Network (CNN) models with three different seeds after data augmentation, we found that among the five traditional data augmentation
techniques, filpping, rotating, cropping, coloring and blurring, flipping would increase the performance of a image classifier under most of the situations. With the simple CNN models, rotating would also perform well, while cropping and coloring did not help with the performance as compared with the dataset without augmentation. Finally, we also discussed some limitations and future work of this study. 

![alt text](https://github.com/XiongjieDai/Data-Augmentation-with-CNN/blob/main/plot.png)

## Conclusion and future work

We notice that the improvement of testing accuracy differs from different CNN models and different seeds.

However, we could still draw some conclusions. First, for similar CNN models without the inception layer including some convolutional blocks, flipping and rotating always perform better than the other three data augmentation techniques. Based on the results with several different seeds, this study suggests that for simple CNN models with several convolutional layers, flipping and rotating, especially rotating, could help with improving the accuracy of a image classifier. On the other side, cropping, coloring and blurring may not be useful.

Second, for the CNN model with convolutional blocks, the SmallNet3, flipping still performs well. The effect of coloring in improving the predicting accuracy has also improved a lot under this situation. For some more complex CNN models, it will be efficient to start from flipping and coloring rather than the other traditional techniques as mentioned in this article.

This study also has several limitations. First, the study only records results after 10 epochs, because with more epochs, some models may face the problem of overfitting. In the future, more choices of hyper-parameters could also be tested. Second, flipping always perform well in improving testing accuracy. However, under using SmallNet2 with the seed to be 1, the training accuracy and testing accuracy may be stuck at 0.5, meaning that the choice of seeds may not be good enough under this situation.

As for the future work, first, this study focuses building CNN models classifying images between two classes. And the future work could be done by extending this study into building CNN models and augmenting data from multiple classes rather than that with only two classes. By generalizing the study with more classes, it would also be worthwhile to check whether the predicting accuracy for each different class has all been improved since one study reported that even though the data augmentation technique would increase the whole testing accuracy, testing accuracy for some specific classes may be sacrificed and decreased greatly. Last, in the future, it would be worthwhile to try more data augmentation techniques, for example, Generative Adversarial Networks (GANs) or some other newly developed techniques, like Sample-Pairing, as well as some combination between different data augmentation techniques, and compare with the traditional data augmentation techniques to see which data augmentation technique is more likely to be the best one that improves the accuracy in predicting labels and whether combinations of data augmentation techniques would perform better than a single one.

Our group has learned a lot by doing this research through knowing further about using Pytorch to exert different data augmentation techniques to process a image, write the Convolution Neural Network and use SGD to optimize the training process.

## Demo
[Cat & Dog Classifier](https://huggingface.co/spaces/yuhe6/final_project)
