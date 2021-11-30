# biweekly-report-6-siju9917
biweekly-report-6-siju9917 created by GitHub Classroom

Pose Estimation, Optical Flow, and Depth Estimation by Simon Julien and Jackson Curry
***This repo will be the same for both Simon and Jackson as we collaborated on all material.***

This repo contains 3 files:
1. PoseEstimationComparison.ipynb

    This notebook implementation and comparison of Google TensorFlow's 3 primary pose estimation CNN models. From our research, these are the three models that are almost exlusively used when performing pose estimation on humans in TensorFlow. Unfortunately, Google has not release source code or tutorials on how these models were made from scratch, but they have release detailed overviews of the papers, theory, and parameters they used to develop and train the models. In this investigation we have implemented all three models from TensorFlowHub's MOVENET (multipose lightning, singlepose lighning, and singlepose thunder). For the multipose lightning we used video data from tiktok dances (with hopes for future application as explained in the document) and multiple live/real-time webcam videos of Simon and Jackson. Then, to compare the models we proceeded to use webcam video from Simon and Jackson for the other two model architecutes. In our comparison we were looking at speed of reduring as body parts move quickly (and blurry) in real-time, and we were looking at the confidence that each trained model had that it was labeling our 17 important body parts correctly. Our conclusions from this implementation and poking and the models returned conclusions that directly match what google has published as the fastst vs. most accurate models.
    
    
2. CodeLive.mp4

    This is the video of us running PoseEstimationComparison.ipynb live so that you can see our webcam's pose estimation in real-time without having to rerun our notebook (but feel free to).

    
3. OpticalFlowAppliedToDashCamSpeedometer.ipynb

    In this notebook we look at using optical flow to create a useful real-world application where we predict the speed of a car based only off of its dashboard camera footage! We used a kaggle dataset that only provided us with 2 dashboard videos (one for training and one for testing).  And then it gave us one txt file where it gave the speed of the car for each frame in the training video.  In this project we first do an introductory data analysis of the 3 pieces of data we were given.  We then create a CNN model where we feed in optical flow images that are created using successive images from the dashboards (to get a sense for how the scenery was changing from one frame to the next).  Finally, we show how our trained network is able to create real-time predictions for the speed of the test car in the mp4 file below. 
    
4. opticalFlowDashboardDemo.mp4
    In this notebook we showcase the final results that our code was able to output for making speed predictions for the test vehicle! We first show the test.mp4 file (this is the file we were given from the kaggle dataset). Second we show our combined_test_output.mp4 file (where we have the original test video mixed in with our optical flow images we have computed.  And also we overlay the predicted speed of the test vehicle as it is driving!).  Finally we show the test_output.mp4 video (which is just the original video with our speed predictions overlayed)
    
