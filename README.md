## Introduction
The objective of this project transferring the style of an image A to another image B. The method used was **Neural Style Transfer**. 

## Method
1. The general approach of neural style transfer is to first resize and normalize the content image and the style image to same ratio. All the operations are done by converting the image to tensor.

2. Then loss functions are defined according to [this](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf) research paper. **L_BFGS** loss function is used.

3. VGG16 model's convolutional layers are used for extracting features from the image. 

4. The loss function is optimized for 10 iterations.

   **NOTE**: Increasing the no. of iterations from 10 to 30 only increases the brightness of image while showing almost zero increase in style of output image.

5. Finally, the resultant tensor is converted to an image.

## Result

| **Content Image** | **Style Image** | **Output Image** |
|-------------------|------------------|----------------|
|<img src="https://github.com/gauravsharma-97/Neural-Style-Transfer/blob/master/Images/japanese_garden.jpg">|<img src="https://github.com/gauravsharma-97/Neural-Style-Transfer/blob/master/Images/picasso_selfportrait.jpg">|<img src="https://github.com/gauravsharma-97/Neural-Style-Transfer/blob/master/Images/output_image.jpg">|

## References
1. [Image Style Transfer using Convolution Neural Networks, Leon A. Gatys et. Al](https://www.cv-foundation.org/openaccess/content_cvpr_2016/papers/Gatys_Image_Style_Transfer_CVPR_2016_paper.pdf)

2. [Demystifying Neural Style Transfer, Yanghao Li et. Al](https://arxiv.org/pdf/1701.01036.pdf#:~:text=It%20fully%20takes%20the%20advantage,artistic%20style%20of%20a%20image.)

3. [Setting hyperparameters](https://towardsdatascience.com/practical-techniques-for-getting-style-transfer-to-work-19884a0d69eb#:~:text=Total%20variation%20loss%20is%20the,noise%20is%20in%20the%20images.)
