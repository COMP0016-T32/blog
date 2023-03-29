---
layout: post
title:  "Term 2 Week 3 - Week 5"
date:   2023-02-12 00:00:00 +0000
categories: update
---

During this period, we started to come up with ideas to implement our final product. We learned more about the technology that we were going to use and attempted to train a model for the final product. At the same time, we successfully implemented the hand jitter correction algorithm and began to test it.

# Took Photos to Train Dance Mat Model

In the lab session, we took photos of the group members doing the four gestures (forward, backward, leftward, and rightward leg movements). For each gesture, 50 photos were taken. This was to ensure that the dataset was large enough so that the trained model would produce accurate results.

# Researched More on Pose Estimation Framework

To find out the most appropriate way to implement the dance mat, we did some research on the best way to recognise gestures. We found out that the limitation of MediaPipe was that the user’s face must be included in the camera in order to estimate the user’s pose. As a result, the users need to put a distance between themselves and the computer, making it hard for them to see the screen. To eliminate the limitation, we read some papers to find alternative ways.
However, we later realised that it was hard to use another pose estimation framework for MI since MediaPipe was already implemented in the legacy codes. Therefore, we decided that MediaPipe was still the most appropriate framework to use for our project.

# Hand Jitter Correction Experimenting

We implemented a hand jitter correction algorithm for smoother cursor movement. We mainly used the Smoother class to capture and past hand position coordinates, which were stored in a buffer as a NumPy array, then apply the smoothing algorithms to the data array. We used Laplacian smoothing and Gaussian filtering techniques to smooth out the tracking points. Laplacian smoothing involved taking the mean of each point and its neighbors, while Gaussian filtering involved applying a Gaussian filter to the tracking points. The smoothing function improved the accuracy and responsiveness of the cursor movement, providing a better user experience.