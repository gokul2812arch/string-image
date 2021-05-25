# string-image
string image art python black white

Inspired by the series of artwork "A new way to knit (2016)"[1] this is a string image , which uses a intricate knitting patterns around fixed pins, with a thin thread to display images instead of pixels. 

A single thread is taken around the pins in a seemingly random arrangement continuously around 1000 - 2000 times. Places where the thread  overlaps or clusters creates a darker tome whereas its absence gives a white color tone. Together the full greyscale palette is represented and their perfect combination gives it the appearance of the desired image.

The pattern is generated through a greedy algorithm in python (see github) which starts a point and then creates the best possible line step by step from one pin to the next, The best line is defined by the line that gives the least error i.e. the line whose average pixels value is the highest .

#Psudocode

1)prepare the image 
load image , resize it to a square , make it black and white 

2) get pins locations 
get the pixel coordinates of the shape in which you want to hammer in the pins 

3) Start making image
get the line with the highest average pixel value,  
line is converted to the pixel coordinates using the bresenham's line algorithm [2] which closely approximates the pixels to be shaded to form a line between two points. 

4) continue iteratively from the last point selected to new point for a long as desired.

Note: The image becomes darker and darker per iteration and if carried out forever the image will just turn black. so it has to be stopped at some point. 1300 iterations gave best result for this image. 

![Alt text](20210526040016.PNG?raw=true "iterations")
