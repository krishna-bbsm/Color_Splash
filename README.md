# Color_Splash
Welcome to Color Splash - the revolutionary software that brings new life to your vintage memories. With our advanced deep learning technology, you can now transform your black and white photos into vivid, full-color masterpieces in just a few clicks


# *COLOR SPLASH - 'Revive your old memories'*

**INTRODUCTION:**
 
 *Colorizing images is a complex task that requires prior knowledge of image content and manual adjustments to achieve artifact-free quality. This is typically done by hand in tools like Photoshop, which is time-consuming and requires a lot of energy. Machine learning and deep learning techniques can be used to automate this process and make it easier.*

** Model **
Download the model through this link:
https://mega.nz/file/tzIyAJZK#l1_iOPulwOApQ2SKBgjyZVtuTFgIX6HOZgnewG4NldM

**OUR PRODUCT:**

*We have developed a user-friendly Python interface that converts black and white images to the best possible colorized images. Our interface uses cv2, PySimpleGUI, and numpy to implement the colorization network. It is easy to use and produces high-quality results.*

**IMPLEMENTATION:**

*1)	Load the input image from disk, scale the pixel intensities to the range [0, 1], and then convert the image from the BGR to Lab color space*

*2)	Resize the Lab image to 224x224 (the dimensions the colorization network accepts), split channels, extract the 'L' channel, and then perform mean centering*

*3)	Pass the L channel through the network which will predict the 'a' and 'b' channel values*

*4)	Resize the predicted 'ab' volume to the same dimensions as our input image*

*5)	Grab the 'L' channel from the original input image (not the resized one) and concatenate the original 'L' channel with the predicted 'ab' channels*

*6)	Convert the output image from the Lab color space to RGB, then clip any values that fall outside the range [0, 1]*

*7)	The current colorized image is represented as a floating point data type in the range [0, 1] -- let's convert to an unsigned 8-bit integer representation in the range [0, 255]*

*8) Save the image in the desired location.




