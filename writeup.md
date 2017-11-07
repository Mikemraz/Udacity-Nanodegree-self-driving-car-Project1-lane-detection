# **Finding Lane Lines on the Road** 

---

**Finding Lane Lines on the Road**

The goals / steps of this project are the following:
* Make a pipeline that finds lane lines on the road
* Reflect on your work in a written report


---

### Reflection

### 1. Describe your pipeline. As part of the description, explain how you modified the draw_lines() function.

My pipeline consisted of 6 steps. 
First, I converted the images to grayscale, 
then I use the gaussian blurring function to make the image more smooth, 
then I use Canny method to detect edges of the image, 
and then I define a polygon and by using the region_of_interest function to find the preferred area,
then I use the hough method to find lines in the interested image, and connect the lines,
at last, I put the marked detected lanes with the original image together.

some changes:
1. for the draw-line() function, I only changed the default thickness to 6, and it works well.
2. I also change the polygon area, as well as hough function's parameters.




### 2. Identify potential shortcomings with your current pipeline


I guess we can build a new polygon to detect the area of the curve of pavement marker, that's not hard. that can address the curve problem.

Another problem is the shadow of trees appear once in a while, and the surface of the road is not consistant compared to previous situation, which is kind of dirty and messy.We might want to build a super complex polyton to exculde everyting except the lane(might work, but with little power of generalization).

But the really hard problem is how we can acommondate this application with our previous work(straight pavement marker). Because in the real world, it would be too tedious to tell the machine when we are driving on a curve or straight line. IN OTHER WORDS, is there a way for us to create a dynamic polygon which can find our perferred area by itself? That's what I am thinking...


### 3. Suggest possible improvements to your pipeline

As I have said, A possible improvement would be to building a new polygon to detect the area of the curve of pavement marker.


