# biweekly-report-4-siju9917
biweekly-report-4-siju9917 created by GitHub Classroom

Biweekley Report 4: Developed by Simon Julien & Jackson Curry 

(ALL CODE WILL BE THE SAME IN BOTH OUR REPOSITORIES THIS WEEK. NO NEED TO READ CLOSELY TWICE.)

In this biweekly report we have two primary investigations that we have taken a deep dive into the implementation based on concepts from class. First we have an investigation into robustness and how to make image classification fail with various attacks. Secondly, we have a look into DeDonvNet and the process of decoding a model to visualize, understand, and defend against noisey (possibly attacked) image data.

Robustness:

In last weeks biweekly report we discussed how we could use model distillation in order to get lightweight models that could run in a realistic amount of time to be used in production while maintaining a high level of accuracy/performance. This week we will be discussing another very important part of any production model which is security and robustness of the model. This matters because in real-world production there will most likely be people who will want to make malicious attacks on software products in order to make them behave in a different way that benefits them. We need to make our models and networks as robust as possible so that these kinds of adversarial attacks don't work very well (in the example above we would want our TSA screening software to be robust to an attack so that the gun would be properly identified and confiscated at security.

In this section we performed adversarial attacks, tarrget attacks, non-targeted attacks, one pixel attqacks and evaluated robustness throughout. This is a constantly developing field where people are constantly going back and forth creating new adversarial attacks while other solve them, and ultimately it is by this process that our network models become more robust. Ultimately, but investigating how different attacks impact that accuracy of classification, we can develop more robust models and NN.


DeConvNet:

In the DeConvNet investigation we were able to answer a question that was linguring between us for a while: Can you process an image back through a NN model and return how the model is interpreting the image? This question was answered in our visualizing and understanding section of class so we were excited to implement. Using the TensorFlow Conv2DTranspose function for deconvnet, we implemented the decoding process on cifar10 in a few different ways with varied complexity of NN. After a thurough preliminary implementation, we used the process to train a model to remain moderately unimpacted by tampered/noisey image data. Our results showed strong accuracy in both cifar10 and mnist, but mnist was particulary impressive because the binary nature allowed the encoding->decoding method to basically remove all noise while maintinaing similar resolution!




p.s. thanks so much for the collab recommendation for GPU. We took some time to familiarize and share work over collab while using the free GPU and our work efficiency was much faster than last week because we could debug faster! At the end oddly "ran out of GPU". Not sure if you have ran into this before, but if you have any further recommendations we would love it!
