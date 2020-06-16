# **Finding Lane Lines on the Road** 

---

**Project1: Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report

---

### Reflection

### After opening the file and reading FPS and frame dimensions my pipeline consists of 9 steps:
	
	1. Read the frame and convert it to grayscale
	2. Run Canny edge detection
	3. Mask out the region of interest
	4. Run Hough transform to detect the lines
	5. Separate left side lane markings from the right side lane markings by slope, filtering out unusually tilted ones
	6. Calculate slope and intercept for each line and store them in lists
	7. Draw the representations using the mean slope and intercept for each side
	8. Overlay the lines on the original image
	9. Display the result in the IPyton widget and write output


### 2. Identify potential shortcomings with your current pipeline

The pipeline works reasonably well even on the "challenge" video, but the output is jittery on the bright section of the road.
Also it processes even curved lines as straight.

### 3. Suggest possible improvements to your pipeline

The first improvement would be to let user specify the input file without editing the script, ex: 
	1. Accept command line arguments
	2. Scan the current directory and let the user choose a file to process
	3. Option to open a camera as input device

Also the input frame brightness/contrast can be normalized to make Canny edge detection work reliable across different lighting conditions.

