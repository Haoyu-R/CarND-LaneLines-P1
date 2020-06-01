# **Finding Lane Lines on the Road** 

## Writeup Template

### You can use this file as a template for your writeup if you want to submit it as a markdown file. But feel free to use some other method and submit a pdf if you prefer.

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I applied a gaussian filter on the image before sending to canny detection, this could depress noise better. Once the canny edges on the images are detected, only the region of interests is remained using a mask. At last, by using hough line transformation the lane lines are found and drawn.

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by averaging the left and right lane separately. 


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when the size of the video is different between frames. This happened when running the algorithm on the challenge video. Also, some outliers may cause the lane drawing unstable.



### 3. Suggest possible improvements to your pipeline

A possible improvement would be to adapt the algorithm that can work for every size of the video.
