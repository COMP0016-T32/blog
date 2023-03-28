---
layout: post
title:  "Term 2 Week 1 - Week 2"
date:   2023-01-22 00:00:00 +0000
categories: update
---
# Added Speech Command for Fifa

To fully support gameplay in FIFA, we added speech commands so that the users would be able to use more features of Fifa. For sprinting in Fifa, we planned to use one speech command to change the game character to sprinting and another speech command to change the game character back to the normal speed. However, we discovered that the speech command would only press the key that the command was mapped to once. In order for the speech command to hold the key, we tried the key_down function in keyboard.py, but it did not work. After researching, we found out that holding the key would require starting a thread. As a result, we implemented new key_down and key_up functions in keyboard.py so that one speech command could hold the key and another speech command could release the key.

# Added Helldivers Mode

As we were given a new game, Helldivers, by Prof Dean, we implemented a new mode for the new game. On top of feet extremities and speech commands, we added area of interest (AOI) to Helldivers. AOI allowed users to control the mouse with their hands and trigger mouse actions such as left click and right click with their hand gestures. It was needed in Helldivers because Helldivers involved aiming and shooting, which could not be achieved with extremity buttons.  

# Added New Displayed Text for Extremity Buttons

Originally, the extremity buttons were displaying the number of the times that the buttons were activated. This did not convey useful information and it was hard for the users to find out the keys that the buttons were mapped to. Hence, we changed the displayed text to the keys that the buttons were mapped to. Initially, it was hard to locate the codes to change as MI had a large codebase, but after hours of analysing, we managed to find the right place to add the new displayed text for extremity buttons.

# Resolved Unstable AOI

While testing the games, we discovered that the gesture detection of AOI was not consistent. More specifically, it only recognised the gesture for the left click for around 60% of the time. We managed to get around of the issue by changing the gestures for the left click and the right click to two completely different gestures as we discovered that the gesture detection of AOI worked better for different gestures than similar gestures, such as pinch the index finger and pinch the middle finger.

# Game Test

We tested the various mode with a variety of games, such as Fifa, Helldivers, Pinball, and Chess. The game test was filmed and sent to Prof Dean to review. 

# Completed Fifa Configuration Wizard

The saving to json files part was added to the codes for the Fifa configuration wizard. This was the final touch of the configuration wizard, and it worked well afterwards.

# Started Project Website

We hosted the project website and added profiles of the group members onto the project website.

# Demonstration to Industrial Partners

We were honoured to show our product to people from PlayStation and Microsoft. When they came to campus, we prepared a presentation to introduce our product to them. We talked about the background of the project and the solutions we proposed, as well as the future work that we planned. Afterwards, we showed clips of us playing games using our product. We also answered the questions from the industrial partners and received feedback from them.

# Elevator Pitch

We prepared the slides and the script for the elevator pitch, which was a two-minute presentation to showcase our product using non-technical terms. We worked together to refine the slides and the script. It was also a chance for us to reflect on our progress and plan for the future work.