# Clustering-And-DeepFakeDetection
In recent months, AI-synthesized face swapping videos referred to as deepfake have become an emerging problem. False video is becoming more and more difficult to distinguish, which brings a series of challenges to social security.
The continuous advancement of video tampering technology and the improvement of video quality have also brought great challenges to deepfake detection.
By this project, we will try to detect if a video is  deepfake or not using Deep Learning Techniques.

# Methodology
1)Converting the input video to frames.
2)Locating face within the frames generated.
3)Data exploration and clustering of images using PCA, T-SNE and DBSCAN for better train test split so that the obtained model learns to resist adversarial examples and optimized input for training.
4)Performing inter-frame analysis on video to detect deepfake directly (in case when only a part of video is morphed). 
5)Using  MTCNN and Inception Resnet models for feature extraction and to make classifications.
6)Choosing the best model on the basis of accuracy scores obtained and making predictions and classifying videos as real/fake.

# Inter Frame Analysis
1)Extract frames from video using cv module.
2)Locating faces in frames using face recognition module.
3)Drawing facial landmarks using face recognitions’s facial landmarks functions.
4)Frame by Frame detection of facial landmarks.
5)Comparing the adjacent frames to detect morphing.

# Test Train Split
From the frames in each cluster, videos corresponding to those frames are mapped and clustered together.
From each cluster 70% of videos goes to train set while the other 30% to the test set.

# Structure of dataset:
Celeb-real # 45 Celebrity videos downloaded from YouTube
YouTube-real # 25 Additional videos downloaded from YouTube
Celeb-synthesis 330 Synthesized videos from Celeb-real (260 from celeb-real) and Youtube real (70 from youtube real)

# Work Done
1)Clustering of frames using following techniques:
  PCA
  t-DSNE
  DBSCAN

2)Inter-frame analysis to detect morphing in certain portion of videos
  MSE
  SSIM

3)Classify video as real or fake

# Results
![alt text](https://github.com/SARTHAK4U/Clustering-And-DeepFakeDetection/blob/main/1.png)
![2](https://github.com/SARTHAK4U/Clustering-And-DeepFakeDetection/blob/main/2.png)
![3](https://github.com/SARTHAK4U/Clustering-And-DeepFakeDetection/blob/main/3.png)
![4](https://github.com/SARTHAK4U/Clustering-And-DeepFakeDetection/blob/main/4.png)
![5](https://github.com/SARTHAK4U/Clustering-And-DeepFakeDetection/blob/main/5.png)



