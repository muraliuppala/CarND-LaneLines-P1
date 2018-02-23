# **Finding Lane Lines on the Road** 

The goal of the project is to develop an algorithm to detect lane lines in an image and video stream. 

---

### Data Processing Pipeline:

I have developed a processing pipeline that works on a series of individual images, and applied the result to a video stream. Implemented the algorithm using Python and OpenCV.

**Pipeline Architecture:**

1. Load the images.
2. Apply Grayscale transform that will only return an image with one channel
2. Apply Gaussian smoothing to the gray scale image to suppress noise and spurious gradients by averaging
3. Apply Canny transform to detect edges.
4. Apply Image masking to extract region of interest.
5. Apply Hough Transform to detect the lines.
6. Prepare a black image on which lane lines will be drawn.
6. Draw the lane line using the approach described below.
8. Combine initial image with lane lines image to get the final result.


[//]: # (Image References)

[image1]: ./examples/grayscale.jpg "Grayscale"

---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I .... 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by ...

If you'd like to include images to show how the pipeline works, here is how to include an image: 

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when ... 

Another shortcoming could be ...


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to ...

Another potential improvement could be to ...
