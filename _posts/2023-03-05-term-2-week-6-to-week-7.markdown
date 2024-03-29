---
layout: post
title:  "Term 2 Week 6 - Week 7"
date:   2023-03-05 00:00:00 +0000
categories: update
---

In these two weeks, we successfully added the virtual dance mat to the MotionInput codebase. Moreover, we added more components to the dance mat and fixed some bugs. We also designed the configuration wizard.

# Added the Virtual Dance Mat

After thoughtful research and compromise with the situation such as time and resources, we decided to use MediaPipe as our core technology. There are relatively a lot of resources available on blogs and YouTube videos. One of the most helpful websites was [Bleed AI’s blog posting](https://bleedai.com/introduction-to-pose-detection-and-basic-pose-classification/). Basically, using the coordinates of the landmarks provided by MediaPipe, I can set the mathematical expression to measure a gesture that we want to capture. For the detailed information about the algorithm, please visit the Research and Implementation section in our [website](https://students.cs.ucl.ac.uk/2022/group32/). With temporary thresholds we set after a few times of testing, we have checked that this implementation can be kept for this project. But it is required to have extensive experiments with various situations like different cameras angles and people in the future.

Unfortunately, however, there has always been a problem with the team that it is very difficult to integrate the new features we created with the existing MotionInput codebase. We have spent more than 5 days trying to put it into MotionInput but failed in the end. Nonetheless, we were able to do this thanks to Team 26’s new holistic module. They made it much easier to embed our codes and maintain them.

Yes! Finally, we have added the virtual dance mat which was our top priority. We really appreciate Abid in Team 26 for helping and encouraging our developers with nice compliments.

# Added the Dance Mat Visualiser

To make the virtual dance mat more intuitive, we planned to add a dance mat visualiser so that the users would get instant information on the status of the four gestures supported by the virtual dance mat. Like extremity buttons, the dance mat virsualisers would contain four buttons for the four gestures, and the buttons would change colour when activated to inform the users that they performed the corresponding gestures successfully. To differentiate the dance mat visualiser from the extremity buttons, the buttons of the dance mat visualiser were square-shaped while the extremity buttons had a circle shape. 

It was challenging to analyse the large amount of codes of MI and found the correct place to implement the dance mat visualiser. Moreover, as we were using a new module to implement the virtual dance mat, we did not have a lot of reference of how the display on the MI window worked. After devoting hours to read the codes, we finally found that the display on the MI window was defined in display_element.py. 

After happily adding a class in display_element.py to define the dance mat visualiser and thinking that we did a great job, we faced a more severe problem. We had no idea how to initialise the class in the dance mat gesture classes. We thought of to follow the same logic as how extremity buttons worked, but we were devastated to find out that simply changing the colour of the extremity buttons when they were activated entails incorporating multiple layers of classes within both the gesture event folder and gesture event handler folder. It would be very hard for us to implement the same logic in the holistic module, which was also unnecessary as most functions defined in these classes were irrelevant to us. After two days of hard thinking, we were blessed with an epiphany that we could create a global class for the dance mat visualiser that initialised the dance mat class defined in display_element.py. We were glad that this method worked.

# Fixed Key Pressing Event for Dance Mat Gestures

After adding the virtual dance mat, we realized that the dance mat gestures were triggering the same effect for action types “key_press” and “key_down”, which was holding the keys mapped to the dance mat gestures when the dance mat gestures were activated. This was problematic as key_press should only press the key once while key_down should be holding the key. After studying the logic of how key_press and key_down were implemented for extremity buttons, we created a new boolean variable in abstract_pose.py, which was where whether the dance mat gestures was activated was determined. The new boolean variable tracked the status of the key_press event, and would be turned true if the event occurred after the gesture was activated. As a result, the key would only be pressed once for the duration that the gesture was activated. In the deactivating stage of the gestures, the boolean variable would be turned to false to get ready for a new activating stage.

# Designed the Configuration Wizard

The configuration wizard (MFC) of the virtual dance mat would be coded using MFC and C++. With the aim of giving the users as much freedom as possible in mind, we brainstormed the design of the configuration wizard together. 

![mfc sketch]({{ site.baseurl }}/images/mfc_sketch.png)

In the initial design, the first page of the configuration wizard showed the preset modes of the virtual dance mat. When clicking on one of the modes, such as FIFA, another page with four buttons, which were Dance Mat, AOI, Speech, and Extremity, would open. Clicking on these buttons would lead to the corresponding pages for setting the components, which allowed the users to customise these components. Moreover, in the first page, the users would be able to add customised modes by clicking the add button, which would lead them to a new page that prompted the users to enter the name for the new mode.

However, after showing our design to Prof Dean, he reflected that our design was too complicated and had a steep learning curve for the users. He helped us to simplify our design.
