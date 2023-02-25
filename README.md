# Color_Splash
Welcome to Color Splash - the revolutionary software that brings new life to your vintage memories. With our advanced deep learning technology, you can now transform your black and white photos into vivid, full-color masterpieces in just a few clicks


# *COLOR SPLASH - 'Revive your old memories'*

**INTRODUCTION:**

*Image colorization is the process of assigning colors to a grayscale image to make it more aesthetically appealing and perceptually meaningful. These are recognized as sophisticated tasks than often require prior knowledge of image content and manual adjustments to achieve artifact-free quality. Also, since objects can have different colors, there are many possible ways to assign colors to pixels in an image, which means there is no unique solution to this problem.*
 
*Nowadays, image colorization is usually done by hand in Photoshop. Many institutions use image colorization services for assigning colors to grayscale historic images. There is also for colorization purposes in the documentation image. However, using Photoshop for this purpose requires more energy and time. One solution to this problem is to use machine learning / deep learning techniques.*

**OUR PRODUCT:**

*We have developed a software with minimal user interface using python and its libraries , that converts b/w images to its best possible colorized image. We use cv2, models implemented with Tensorflow , pysimpleGUI, numpy for this project.*

**CORE IMPLEMENTATION:**

*1)	load the input image from disk, scale the pixel intensities to the range [0, 1], and then convert the image from the BGR to Lab color space*

*2)	resize the Lab image to 224x224 (the dimensions the colorization network accepts), split channels, extract the 'L' channel, and then perform mean centering*

*3)	pass the L channel through the network which will predict the 'a' and 'b' channel values*

*4)	resize the predicted 'ab' volume to the same dimensions as our input image*

*5)	grab the 'L' channel from the original input image (not the resized one) and concatenate the original 'L' channel with the predicted 'ab' channels*

*6)	convert the output image from the Lab color space to RGB, then clip any values that fall outside the range [0, 1]*

*7)	the current colorized image is represented as a floating point data type in the range [0, 1] -- let's convert to an unsigned 8-bit integer representation in the range [0, 255]*

*8) Save the image in the desired location.




