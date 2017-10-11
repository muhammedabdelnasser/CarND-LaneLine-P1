# **Finding Lane Lines on the Road** 


### This project is to detect and find the lane lines of the road. This project is using Hough transform, Canny edge detectionm and linear regression to identify and mark the lane lines  of the road.

---

## How it works

- Detect the lane lines.
- Fit a curve to the points that make the line
- Draw the red lines on top of the lane lines

---

**Finding Lane Lines on the Road**

The goals of this project are the following:
* Find and detect the lane line on the road.
* Draw up the detected lines on images and videos.

The steps of this project are the following:
* Read and load the iamges form the drive.
* Convert the image from color to grayscale image.
* Apply the gaussian blur filtering mechanism.
* Apply the Canny edge transform to find the edges.
* Select and apply the region to process.
* Apply the Hough transform.
* Make stripped lines connected.
* Draw the detected lines on the image or video frames.


[//]: # (Image References)

[image1]: ./test_images/solidWhiteRight_detected.png "Detected Lines"
[image1]: ./test_images/solidYellowLeft_detected.png "Detected Lines"

---

### Reflection

### 1. Pipeline.  draw_lines() function modification tp draw_lines_connected().

* Detect the slope and intercept of the points on identified.
* Find the maximum slope and min slope of the lines on the image, to be able to identify the left and right line.
* Separte the two lines to left and right.
* Find the line that passes with all the left and right points and draw it.


### 2. Identify potential shortcomings with your current pipeline

One potential shortcoming would be what would happen when the road have curves. 


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to use the 2nd order interpolation to fit all the points we have including the curves on road lane lines.