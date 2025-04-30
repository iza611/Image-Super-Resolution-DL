Deep convolutional neural network (DCNN) is a learning-based approach, as opposed to traditional methods where the algorithms were hand-crafted. With deep learning, the extraction of patterns happens automatically and is able to capture more complex patterns. For image super-resolution, DCNN learns relationships between high-resolution and low-resolution images with provided training examples. It identifies patterns that can be generalized for unseen examples. DCNNs are particularly well-suited for image data, thanks to their convolutional layers that can extract features related specifically to images, such as illumination, corners, texture, edges, and other visual patterns. When the trained model is used on a new image, it can use its knowledge of previously seen training images to transform the image to a higher resolution. DCNN can quickly and accurately deal with a process that for a human designer is difficult and tedious. 

example pixels calculation
Suppose the settings of a SRCNN as: f1=9, f2=3, f3=5, such a network utilizes (9+3+5-2)^2 = 15^2 = 225 pixels of the low-resolution image to reconstruct a pixel in the high-resolution image.  

![Alt text](https://i.imgur.com/6IEKzja.jpeg)
<img src="readme_imgs/PSNR_MSE.png" alt="Alt text" width="300"/>

f and g – matrix data representing the ground truth image and the enhanced image, respectively 
R – maximum value in the ground truth image (usually R = 255) 
MSE (Mean Squared Error) – average of squared differences between corresponding pixel values in f 
and g 

The PSNR is calculated as the ratio between the peak value R and the mean squared error between 
ground truth image and image produced by the super-resolution algorithm MSE. The logarithm is 
used to compress the dynamic range values, making it easier to compare across different image sizes 
and pixel values. This also results in scores that are represented as more convenient, smaller numbers. 
PSNR can be used to calculate similarity between ground truth image and the one produced by the 
super-resolution algorithm. This way, the effectiveness of the algorithm can be evaluated. The higher 
the PSNR value, the closer the enhanced image is to the ground truth image.  

Results 
[GT - ground truth; HR-Base - interpolation; HR-SRCNN - DL upscale](results/results.pdf)
![alt text](https://github.com/iza611/Image-Super-Resolution-DL/blob/main/results/results.pdf)
