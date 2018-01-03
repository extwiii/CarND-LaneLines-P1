# **Finding Lane Lines on the Road** 



The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


[//]: # (Image References)

[image1]: ./test_images_output/solidWhiteRight.jpg

---

### Reflection

My pipeline consisted of 5 steps. First, I converted the images to grayscale, then I implemented Canny Transformed 
algorithm and masked our region of interest. 

In order to draw a single line on the left and right lanes, I modified the draw_lines() function by finding slope and 
getting every points we have on image in order to implement numpy polyfit and poly1d function to find our lines for given image.

While implementing our draw_line function we also draw red line with line function of cv2.

Last but not least we masked these lines over original image and got below image fro result:

![alt text][image1]


### 2. Identify potential shortcomings with your current pipeline


One potential shortcoming would be what would happen when there is no road line. We are depending on road lines to decide how
to draw our lines.

Another shortcoming could be different weather condition like very sunny or heavy rain, that might make hard to draw our lines
over road


### 3. Suggest possible improvements to your pipeline

A possible improvement would be to depending on road rather than lines, deciding if we have ridable road or not.

Another potential improvement could be to use different sensor to recognize road lines in order to avoid weather conditions.
