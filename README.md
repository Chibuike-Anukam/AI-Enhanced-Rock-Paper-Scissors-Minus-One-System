# AI-Enhanced-Rock-Paper-Scissors-Minus-One-System

This project was the final project in one of my AISE courses, AISE 3350 Cyber-Physical Systems. 
The idea behind this project was to create a system that could play the classic game Rock-Paper-Scissors-Minus-One by predicting the most likely gesture of the opponent and suggesting to the user what gesture to remove to maximize the possibility of winning (search up how Rock-Paper-Scissors-Minus-One is played to better understand how it works!). 

The pipeline is as follows: A top-down image of two players with two gestures each (one for each hand) is uploaded. The ML model (YOLO) uses object detection to read the gestures from the image. Game theory rules are applied to determine which gesture the user (the person whose hands are facing upwards in the image) should remove, and the suggestion is visually displayed. 
