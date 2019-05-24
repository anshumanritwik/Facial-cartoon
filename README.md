# Facial-cartoon using OpenCv and Scikit learn

This project is based upon generation of facial cartoons from base image and adding any animated background to the image.

The facial cartooning pipeline can be broken down into three parts.

## 1. Image resizing

* Depending upon the source of the image, the image size will vary which affects the final image in terms of dimensions. To prevent this, the input image(s) are subjected to resizing using a fixed height and a width proportional to the width.

* The output is a set of images having similar dimensions which is sent for face detection.

## 2. Face detection and cropping from the input image.

* The input image is now subjected to a frontal and profile face detection using the HaarCascade_frontal and HaarCascade_profile respectively.

* Detected faces are cropped and stored separately.

## 3. Facial Cartoon

* The facial cartoon has been obtained in two different ways. The underlying idea in both the technique is the same.
  
  * Subjecting the image to thresholding to obtain edges.
  * Subjecting the original image again to a mask generation/ segmentation code snippet.
  * Imposing the edges and the mask/ segmented image on top of each other with opacity as per requirement.
  
  ##### 1. Facial cartoon using Mask generation
    - The mask generation process involves extracting the part of the image which is lying between a certain color range and then   filling it up again using the color of your requirement.
    - The obtained mask is then imposed over the image containing the edges of the original image.
    
  ##### 2. Facial cartoon using Segmentation
    - The original image is segmented and then the edges of the original image obtained by thresholding are imposed on top of it.
    
## 4. Animations

* Any animations created in this project are based entirely on Python's game development library pygame.

* Using pygame, the images are successively loaded to generate sprites.

* These sprites serve as the reel for the animations.



#### Cartoon using segmentation - cartoon_bysegmentation.ipynb

#### Cartoon using mask generation - maskgenerated_facialcartoon.ipynb

#### face detection using haarcascade - face detection.ipynb

#### Animation (snowfall) - swiping movement.ipynb
