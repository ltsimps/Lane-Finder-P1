Finding Lane Lines on the Road

##Writeup Template

##Finding Lane Lines on the Road

- The goals / steps of this project are the following:

- Make a pipeline that finds lane lines on the road
- Reflect on your work in a written report
- Reflection

1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

The program  pipeline followed the process laid out during the lecture and consisted of the following  steps. First, I converted the images to a HSV colorspace the color yellow in the image, then defined the parameters for masking. After that I detect edges with a canny filter and figure out which are lines using a hough transform by tuning the parameters.  Using a kernel size of 7 for Gaussian blur to make groups with near yellows and whites points. After processing lines the algoirthm is tested on the videos

2. Identify potential shortcomings with your current pipeline

Yellow and white lines aren't covered consistently and it does horrible on curved lines.

3. Suggest possible improvements to your pipeline

A possible improvement would be to come up with a different region masking algorithm so it does better on curved lines. Perhaps using some sort of filer on the image that detects curved lines would help. The downfall would be picking up curves in the image that weren't traffic lines but the filtering done to detect traffic lines should help. Although there could be false detection of white lines in some images that weren't traffic lines.

