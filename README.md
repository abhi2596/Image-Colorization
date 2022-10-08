# Image-Colorization

Used CNN to colorize images. Developed a model based on the architecture given below 

![image](https://user-images.githubusercontent.com/80634226/194685477-17725c11-a67b-4e24-9552-5788f3826cb4.png)

This architecture was taken from https://tinyclouds.org/colorize.

Used a pretrained VGG-16 model and added few layers so as to colorize the images. The network was trained on Flickr 8k dataset. The images in the dataset were color images so had to preprocess the images to LUV colorspace and extract the L channel and feed it to the network as input. The L channel in LUV color space represents the 
luminance and when viewed gives a black and white image. As VGG16 network requires the image to be of 3 channels we stack the L channel. Then the output of the network
is U and V which when concatenated with L channel gives a color image.
