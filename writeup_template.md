# **Finding Lane Lines on the Road** 

The goal of the project is to develop an algorithm to detect lane lines in an image and video stream. 

---

### Data Processing Pipeline:

I have developed a processing pipeline that works on a series of individual images and applied the result to a video stream. Implemented the algorithm using Python and OpenCV.

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

---

### Averaging and Extrapolating the lane lines:

I have taken two approaches to map out the full extent of the lane.

**Approach 1:**
Separating line segments by their slope to decide which segments are part of the left line vs. the right line. Then, you can average the position of each of the lines and extrapolate to the top and bottom of the lane.

**Approach 2:**
Divided the image vertically into two parts. Separating line segments by their position in the image to decide which segments are part of the left line vs. the right line. Extrapolated the lines using numpy.polyfit.

### Shortcomings:


### Improvements:
