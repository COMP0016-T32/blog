---
layout: post
title:  "Term 2 Week 3 - Week 4"
date:   2023-02-05 00:00:00 +0000
categories: update
---

# Took Photos to Train Dance Mat Model

In the lab session, we took photos of the group members doing the four gestures (forward, backward, leftward, and rightward leg movements). For each gesture, 50 photos were taken. This was to ensure that the dataset was large enough so that the trained model would produce accurate results.

# Researched More on Pose Estimation Framework

To find out the most appropriate way to implement the dance mat, we did some research on the best way to recognise gestures. We found out that the limitation of MediaPipe was that the user’s face must be included in the camera in order to estimate the user’s pose. As a result, the users need to put a distance between themselves and the computer, making it hard for them to see the screen. To eliminate the limitation, we read some papers to find alternative ways.
However, we later realised that it was hard to use another pose estimation framework for MI since MediaPipe was already implemented in the legacy codes. Therefore, we decided that MediaPipe was still the most appropriate framework to use for our project.
