# CS580S2022

## Assignment 9

### Working Outline of Final Delivable

#### Name

Garrison Vanzin

#### GitHub Account Name

gvanzin-allegheny

---
```
1.  Area of Research : 
      - Image Classification
      - Neural Networks
      
    Proposed Idea : Neural network that can seperate videos into categories based on similarity.
      - Important for data organization
      
2.  Image classification models
      - Dall-E
      - CoCa
      - CaiT-M
    Convolutional Neural Networks
      - Optimized for image classification
      
    Goals for project : 
      1. Learn more about convolutional neural networks.
      2. Develop network to classify videos.
      
3.  Lots of image classification, not as much video classification.
      Ex) Youtube search recommendation, which can be faulty
      
    The reason for the gap :
      > Videos have many changing scenes making finding similarities more complex compared to single images.
      
    Solution for gap : 
      > Find a way to compare objects and content in one video with another.
      
4.  Research Questions : 
      1. "How to train an AI to recognize differences between videos?"
      2. "How to format frames from a video into a single piece of data to input into a neural network?"
      
5.  Scope: Variable scope depending on accuracy wanted and the training dataset size associated with it.
  
    Feasibility: Since project will be a basic version of my idea the scope will be smaller than a more complex model.
      - There are two reasons for creating a more basic model : 
          1. Computational limits
          2. Time Constraints
          
6.  Prototype : A tool to download types of videos from youtube and extract a set amount of frames from each video.

      Design : Terminal interface with options presented to user to run.
      
      Libraries used : 
            1. youtubesearchpython
            2. opencv-python
            3. youtube-dl
            4. yt-dlp
            
7.  Reasoning for prototype : 

      - Will need video data for training the AI.
      - Will need an efficient tool to extract frames from the video data.
      - The prototype makes organizing the data much faster than doing it manually.
      
8.  Experiment : "What type of image processing algorithm should I create to use on the frames from my prototype in order to train my network correctly?"

      Ideas:
            1. Average frames together to check for similarities in color between the videos.
            2. Get the difference between frames to check for similar changes in shape and camera movement in the videos. (content in video)
            
      - With these ideas, I developed two models to check both the average color in a video and the shape changes in a video.
      
      - Used generated image data for the experiment to test simpler data first.
      
9.  Experiment Results : 20 Training Stages
      Color checking AI accuracy : 100%
      Content checking AI accuracy : 96%
      
      - With these results, my ideas for checking the similarities in videos seemed to work, so I moved onto the next part of my project.
      
10.  Experiment Visualization : Screenshots of training output results
      
      - Shows accuracy and loss of each step in the training process.
      
11.  Ethical Concerns

      1. Training relies on using data that is not owned by the developer.
      2. A more powerful version of this project could be used for censorship or misinformation by scanning for and removing videos online.
      
      - Issue 1 could be solved by filming training data yourself rather than downloading videos online.
      - Issue 2 has no permanent efficient prevention measure as solutions to the issue could be reversed.
      
12.  Next Steps : 

      1.  Improve the model
            - Black and white conversion of content model data to prevent issues with color in frames appearing (Perhaps performing edge detection on frames)
            - Average the frames for the content model training dataset
            - Train with more data
                 > More videos
                 > More frames loaded per video
      
       2.  Better Interface
            - Implement a GUI for easier use of the network for training and testing purposes
```
---


(Did you remember to add your name and GitHub account name and date to the top of this document?)
