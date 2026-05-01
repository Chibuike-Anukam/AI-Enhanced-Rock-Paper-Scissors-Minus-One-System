# AI-Enhanced-Rock-Paper-Scissors-Minus-One-System

This project was the final project in one of my AISE courses, AISE 3350 Cyber-Physical Systems. 
The idea behind this project was to create a system that could play the classic game Rock-Paper-Scissors-Minus-One by predicting the most likely gesture of the opponent and suggesting to the user what gesture to remove to maximize the possibility of winning (search up how Rock-Paper-Scissors-Minus-One is played to better understand how it works!). 

The pipeline is as follows: A top-down image of the hands of two players, each with two gestures (one for each hand), is uploaded. The ML model (YOLO) uses object detection to detect gestures in the image. Game theory rules are applied to determine which gesture the user (the person whose hands are facing upwards in the image) should remove, and the suggestion is visually displayed.

The report is also in this repo as well. It goes over how we created our dataset, the preprocessing involved, how ML and computer vision were used, the methods of game theory and decision-making that were used, and issues and solutions. Of course, there is the entire code implementation at the end of the Jupyter Notebook as well.
*** In the last code cell, on line 4, change the number of the image to the ones listed in the text cell directly above it to see how well the model does in different game scenarios. It should be self-explanatory on how to do this, but just in case! 

The main takeaway from this project for me was realizing how much work it takes to make a good dataset. I spent a total of 10 hours over the course of this project on preprocessing. We, being adventurous, decided to make our own dataset instead of just using one from the web. The ones online were mono-racial (one race) and didn't have game scenario-based images (4 hands with gestures). 
So...... we made our own (real engineering of us, I know)! 
Across the 5 of us, we took over 2500 images. I knew we would have to hand-label all of them, which would have taken forever. So I hand-labelled about 100 of them and trained a small YOLO model on them to autolabel the rest. It was able to label a good amount correctly, but it labelled most of them incorrectly (hence the small dataset of 100 images). As the project deadline approached, we decided to just use whatever images were labelled correctly to train the final model. In the end, we had a decent validation accuracy. We discuss our findings more in depth in the report. 


Overall, this was a great project! I learned a lot about preprocessing and model training. 
The next step would be to finish the labelling of our entire dataset. Quality, labelled data is difficult to find, and I know we would have appreciated having access to a diverse dataset. So I plan to continue to use the small model to auto-label the images. I'm going to hand-label the images that the model labels incorrectly. Then I'll pass them and the images that the model labels correctly back into the model to learn better classification. After, I'll have the model auto-label a small batch of images. I'll repeat this cycle until all the images are done. Hopefully, the model will get better over time, so I won't have to hand-label a lot of images! 
Finally, I'll upload the full dataset, with a test-val (60-40) split, to RoboFlow and/or Kaggle or something. I'll add a link to it in this repo when it's ready. 

Until next time, y'all, take chances, make mistakes, and get messy! (Yes, I was a Magic School Bus fan) 
