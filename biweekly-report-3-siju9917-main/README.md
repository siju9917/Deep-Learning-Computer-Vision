# biweekly-report-3-siju9917
biweekly-report-3-siju9917 created by GitHub Classroom


For this weeks bi-weekly report Simon Julien and Jackson Curry have again worked together to investigate AutoML, Transfer Learning using pre-established neural architectures that match those that we learned about in the papers from class, and knowledge distillation. 

1. Neural Architectures vs AutoKeras
This investigates the packages within TensorFlow that have pre-established model architectures and weighting that are widely acredited (and we saw in class). To integrate these models into more concepts from class, we implemented "transfer learning" that allowed these architectures (initially designed for imagenet) to be compared with our AutoML, previously implemented convolutional NN, and we were hoping knowledge distillations with teacher student training. This file contains the Transfer learning component

2. vs_AutoML_AutoKeras
This is the shorter implementation continuing from the previos file detailed on autoML of tensorflow which is autokeras. This implementation showed why autoML is useful, and when you would want to avoid it due to its extensive training necessary for reasonable performance.

3. Knowledge Distillation 
Our most thurough implementation of the report. In this file we look at how knowledge distillation can be used to transfer the knowledge gained by large complex models into smaller models with less parameters that can be great for production use cases where you need a short run time but high accuracy results.  We first make a general implementation.  Then we look into how the temperature and alpha hyperparameters within knowledge distillation can be optimized to get great results.  Finally we look at how generalizable this process is across datasets by transferring our "optimized parameters" from the MNIST dataset to the CIFAR10 dataset.  Then at the end we talk about possible future directions we are thinking of taking this topic of knowledge distillation in future weeks and ask for advice on how to proceed!

Side Note: This report contained took a lot more time than others due to extensively long trainging and thus increased difficulty in debuging and developing. We are looking into getting GPU for our macs so that we can significantly increase these computational speeds for next time.
