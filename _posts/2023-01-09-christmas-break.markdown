---
layout: post
title:  "Christmas Break"
date:   2023-01-09 00:00:00 +0000
categories: update
---

# Added Feet Extremity Buttons

We were tasked with an additional task by Prof Dean in the Christmas break, which was to find a solution to allow users to play games with their feet. After discussing with and learning from Team 26, we decided to add feet extremity buttons to complete the task. These extremity buttons tracked users’ ankles and would be activated if the coordinates of the users’ ankles were the same as the coordinates of the buttons. As a result, users would be able to play games by overlapping their ankles with the buttons in the MI window.

# Added Kick Extremity Button

Prof Dean had asked us to implement a kicking gesture. However, after we learned how to add a new gesture event from Team 26, we faced difficulties adding a lower body gesture. This was because the new gesture event needed to be added in gestures.json to be recognised, but gestures.json only contained hand primitives, which meant it could only be used to add hand gestures. We could not find a way to add lower body gestures in gestures.json, so we decided to add a kick extremity button that was higher than the other extremities so that when the users activate the button with their ankles, they had to lift up their leg, which mimicked a kicking gesture.

# Created Fifa Configuration Wizard

A configuration wizard was coded in MFC and C++. The configuration wizard allowed the users to choose to play Fifa using their upper body or lower body, customise the phrases used for the speech command, and adjust the kicking strength of the kick button. The layout of the configuration wizard was created and an image of Fifa was added to the configuration wizard. 
