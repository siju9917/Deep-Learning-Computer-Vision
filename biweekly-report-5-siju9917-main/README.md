# biweekly-report-5-siju9917
biweekly-report-5-siju9917 created by GitHub Classroom



This weeks biweekly report between Simon and Jackson contains the following 4 files (same for the both of us):

UNet_investigation.ipynb
Proceeding lecture on image segmentation and our previous work on encoding/ decoding architectures in our last bi-weekly report, we are looking to understand these major topics through performing a dive into U-Net. U-Net in particular has some very interesting applications into medical imaging (for which it was designed), autonomous vehicles, geo sensing, precise architectural planning, and more! Later on we perform U-net image segmentation for a biological imaging dataset. This notebook will contain an initial tutorial-esk implementation of U-Net with the oxford_iii_pet dataset and then a biological application of U-net image segmentation with variant architectures from the origional U-net based on a 2012 image segmentation competition.

Dogs_Vs_Cats_Transfer_Learning.ipynb
In this notebook we investigate a new dataset where one is tasked with classifying dogs and cats.  Much of the difficulty with this section was processing the images that were given in the dataset.  Unlike the Cifar-10 and MNIST datasets where the data is already clean and everything is the same size, this new dataset had images of different size and other weird caveats!  In this notebook we load in the convolutional portion of the VGG16 network that has been pretrained using the massive imagenet library.  We then adapt this network to our current problem by adding layers onto the end such that it outputs 2 classes (dog or cat) instead of 1 of 10000 options for imagenet.  We then train this subset of weights in the network using the current dataset.  We show that using transfer learning we are able to achieve an accuracy of 97% after just a single epoch of training!  This means that the VGG16 network definitely learned something about cats while being trained on imagenet and we were able to transfer and apply this learning to a new dataset with a new purpose.  

Finally we show how to save a specific model that worked well/took a long time to train so that you can have replicable results without having to retrain a massive model.  In the future we want to test another dataset with objects that aren't as common in the imagenet dataset and see if the pretrained VGG model is still able to produce good results through transfer learning (this will answer the question of how careful we have to be to check that the pretrained network has been trained on related objects to your current task)


Transfer_Learning_Knowledge_Distillation.ipynb
In this notebook we extend the knowledge distillation investigation that we completed in a previous week.  We investigate if we can apply transfer learning using VGG16 pretrained on imagenet to act as a new teacher model.  We then use this new teacher model to train a much smaller distillation model and compare the results to the previous week.  This work is still work in progress and not a finished product yet.

Pytorch.ipynb
is week we realized that pyTorch is common in image segmentation. Since we have already been interested in trying some pytorch, we quickly followed a tutorial after finishing our other notebooks from this weeks biweekly report. This pytorch notebook is somewhat brief and follows very closely the tutorial from https://pytorch.org/tutorials/beginner/basics/data_tutorial.html but will be usefull as reference and experience if we need to read or implement Pytorch in the future reports. 
