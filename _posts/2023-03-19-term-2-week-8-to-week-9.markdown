---
layout: post
title:  "Term 2 Week 8 - Week 9"
date:   2023-03-19 00:00:00 +0000
categories: update
---

In these two weeks, we implemented and continued to improve the configuration wizard. We started to wrap up the dance mat and test it with a range of games. We were honoured to have the chance to showcase our product at GOSH.

# Improved MFC

We continued to improve the MFC graphical user interface over the two weeks. To resolve the difficulties of passing the values of variables between dialog windows, we created a GlobalStatus class, which was a singleton class that was referred to in every dialog window class. This singleton class made the development of MFC much easier and more efficient. 

We added various features to refine MFC. First, we added two modes for MFC, which allowed users to select existing controller templates in retro mode or create their own controller templates in modern games mode. Moreover, we added start and select buttons in retro games controller templates so that the users could start the games using FeetNav features. Display input fields were added to the extremity dialog window so that the users could customise the displayed texts on the extremity buttons. We also gave users the choice to use their left hands or right hands to control the extremity buttons.

As suggested by Prof Dean, we changed the names of some components so that they were more intuitive. Extremity was changed to in-air action buttons and AOI was changed to mouse tracking. The new names would be used in future sections.

# Game Test

We tested the usability of the FeetNav features with a variety of games. This was done by playing the games using the virtual dance mat and in-air action buttons. The gameplay was recorded and sent to our project partner. Other than that, we ranked the games in terms of playability with the FeetNav features so that we could evaluate the advantages and the limitations of the FeetNav features.

# Demonstration at Great Ormond Street Hospital for Children (GOSH)

At GOSH, we were blessed with the opportunity to showcase our product to hospital workers and researchers and get feedback from them. The majority of the users who tried our product at the demonstration saw the potential of our product and agreed that it could be applied in hospitals and care homes, which were our intended audience. However, they also pointed out some aspects that could be improved. These aspects included improving the appearance of the in-air action buttons, which was not intuitive, and creating a mouse mode for our product so that it could be used in other activities than gaming. We appreciated their feedback and made plans to improve our product.

# Added Mouse Mode

Following the feedback we received at GOSH, we created a mouse mode for the FeetNav features. This mode allows users to control the mouse using their feet and one arm. When the users move their feet in four directions (forward, backward, leftward, and rightward), the mouse cursor moves horizontally and vertically. The in-air action buttons trigger the left click, right click, scrolling up, and scrolling down mouse actions. 

# Improved the Appearance of the In-Air Action Buttons and Dance Mat Visualiser

To make the in-air action buttons more intuitive, we redesigned their appearance. In the new design, the buttons have a 3D look, and are light blue when not pressed and light yellow when pressed. This made the buttons much more aesthetically pleasing. When combining the images of the new design with existing MI codes for the in-air action buttons, we experienced some difficulties as the activation areas of the buttons were larger than the images. After a few hours of debugging, we found that the activation areas could be decreased in config.json, and thus we managed to resolve the problem.

Moreover, as the users suggested that it was hard to see the black text on the dark blue squares of the dance mat visualiser when it was activated, we changed the colour of the text to white when the dance mat visualiser was activated so that it was clearer.
