# Gesture-Controlled-Flappy-Bird-using-Fist-Detection-Model-with-CNN

### INTRODUCTION
The purpose of the project was to create model which can detect if video from camera contains clenched fist. Based on final model I improved my first project with functionality that give opportunity to play Flappy Bird based on video from camera. The project is divided for three sections: data preparation, training model and flappy bird game. 


### DATA PREPARATION
Firstly I captured 90 self-portraits under varying conditions, including different lighting, camera distances, and angles. It was crucial for me to maintain a clenched fist in some of the shots. Additionally, I could have further enhanced the results by taking pictures in different settings with unique backgrounds. Unfortunately, since I took all the photos in the same location, the model did not perform accurately in different environments. I have included a few sample shots for your reference below.
 
Next, I had to label my photos to distinguish between clenched fist and non-clenched fist images. To achieve this, I utilized the !labelme library, which aided in marking specific areas on the photos. Additionally, I used the Albumentations library to introduce a range of modifications to the images, thereby increasing the diversity of my dataset. The following features were incorporated to achieve this objective:

•	alb.HorizontalFlip(p=0.5) - This transformation horizontally flips the input image with a probability of 0.5

•	alb.RandomBrightnessContrast(p=0.2) - This transformation randomly adjusts the brightness and contrast of the input image with a probability of 0.2

•	alb.RandomGamma(p=0.2) - This transformation randomly adjusts the gamma of the input image with a probability of 0.2

•	alb.RGBShift(p=0.2) -  This transformation randomly shifts the values of the red, green, and blue channels of the input image with a probability of 0.2.

•	VerticalFlip(p=0.5)] - This transformation vertically flips the input image with a probability of 0.5.
On the left side you can see example of modified photo which is the same photo from previous example on the left side. Thanks to that part from 90 photos I got 900. It give us more diverse data set. 



