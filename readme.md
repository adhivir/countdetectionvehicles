ADHIVIR SINGH RANA      101866009       CS3

NOTE:THE CODE IS AVAILABLE IN IPYNB FILE AS WELL AND THE SCREENSHOTS OF I/O AND METHODOLOGY IS PRESENT IN THE FOLDER.

In this project, we will be working on detecting and counting vehicles in a given image. We will be using OpenCV for image processing and Haar cascade which is used for object detection.
We will apply GaussianBlur to remove the noise from the image. Instead of a box filter consisting of equal filter coefficients, a Gaussian kernel is used. It is done with the function, cv2.GaussianBlur(). We should specify the width and height of the kernel which should be positive and odd.
Then we will dilate image. It is just opposite of erosion. Here, a pixel element is '1' if atleast one pixel under the kernel is '1'. So it increases the white region in the image or size of foreground object increases.
Now we need car cascade to detect cars. So, we first need to upload them to collab and then specify the path to car_cascade_src. OpenCV provides a training method (see Cascade Classifier Training) or pretrained models, that can be read using cv2.CascadeClassifier() method. We need to detect multiple objects i.e. cars so we will use detectMultiScale. Detects objects of different sizes in the input image. The detected objects are returned as a list of rectangles.
Now we will use the above returned contours and draw a rectangle around detected cars. Here we will see that it will create the rectangle with red boundary around each and every car it detects.
And then we can count the vehicles.
