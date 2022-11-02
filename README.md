# VidClass

**VidClass** is a experiment designed in Python through Jupyter that attempts to classify a set of videos into categories based on content they have in common.

The motivation for this project stemmed from the gap in the amount video classifiers compared to image classifiers.  One example of a video classifier that many people know about is youtube’s search recommendation algorithm.  You can type in a keyword or phrase for a video and it will find you videos with content similar to the phrase you have given.  However, you can only use words with youtube to find videos, while the main goal of this program is to input a video and then gather similar videos.

## Process

The program uses a convolutional neural network to classify the videos.  To gather data to use as input for the network, two methods are used:

- **Method 1** : Average all the frames of each video together into one average frame per video.  This would condense a whole video into a single image and massively increase training speed.  The other motivation for averaging the frames was to detect color similarities within videos.  For example, if one video’s average frame was more on the blue side, then a video with an average frame on the red side is not similar to the other.  

- **Method 2** : Calculate the difference between elements in a frame’s array from the next frame in the video sequence.  This would hopefully allow the network to detect changes in shapes based on time and also spot the speed the video is playing at.  If a video is shot with a quick pace, the difference between the frames will be much greater compared to a video that is still.  

The diagram below provides a visual way to understand method 2:

![Diagram](https://user-images.githubusercontent.com/54772966/169022253-53f2f16a-8ea5-4a9e-8c29-8afb0d5c3123.png)

## Dependencies

**Dependencies Used for Project** :

- https://opencv.org/releases/

- https://pypi.org/project/youtube-search-python/

- https://github.com/yt-dlp/yt-dlp

- https://github.com/ytdl-org/youtube-dl

## Dataset

The dataset used to originally train the model can be downloaded at the link below.

https://drive.google.com/file/d/1UB_7fQ5gY-xyhWB_gtJul6s8h4O5iArV/view?usp=sharing

The content of the dataset is frog, dog, and cat videos modified using the methods in the process section of the readme.  There are around a total of 28 videos in each category.  The original training of the network used these videos to detect whether a test video belonged in the frog, dog, or cat content category.