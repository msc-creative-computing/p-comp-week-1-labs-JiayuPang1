## Final Work
# Train StyleGAN on a custom dataset
-------------------------

## 1. Background:
#### Generative Adversarial Networks (GANs) are a recent innovation in machine learning, first proposed in 2014 by Ian J. Goodfellow and colleagues. 
#### It is a set of neural networks that play against each other in the form of a two-player zero-sum game.
#### There are several GAN variants currently on the market, but in this research I focused on learning and applying StyleGAN, 
#### which was introduced by Nvidia in December 2018. The architecture of StyleGAN uses a baseline progressive GAN. 
#### That is, the size of the generated images is gradually increased from a very low resolution (4 × 4) to a very high resolution (1024 × 1024), 
#### and bilinear sampling is used instead of the nearest neighbors used in the baseline progressive GAN on/ downsampling.


## 2. Training points:
#### Through self-research and reading materials, I found some key points when using StyleGan to train on my own dataset:
#### (1)	GPU must be used. Since Mac computers do not have GPU, I chose the "google colab" environment recommended by the professor for experiments and learning.
#### (2)	During the training process, a very important point mentioned in all the tutorials is the version of Tensorflow.
####      StyleGAN only works with tf 1.x.
#### (3)	StyleGAN training takes a lot of time. Even though my dataset only has 120 raw images of 128*128, 1024 pixels 
#### (I trained for about a whole day, which also crashed due to usage limitations and timeouts in colab) .
#### I ended up ordering the Colab Pro, and while the training speed did improve, it seemed that the disk memory was filling up quickly.


## 3. Difficulties and methods:
#### When running the code, there were some problems that affected the successful operation, which were finally successfully solved by searching for information and trial and error.

####(1) Run the following code on colab and find that the GPU cannot be found
111111
#### Solution: In colab's "Notebook Settings", find "Hardware Accelerator" and select "GPU"

#### (2) How to read the picture set?
####     a. Upload directly to colab
####     b. Upload to google drive
####     Then copy its file path (note that the file must be a compressed folder)

#### (3) In the code below, the dataset_path I entered keeps showing an error that the file cannot be found.
1111111
####     Note: The file path to be copied here refers to the path to the automatically generated folder in colab. 
####     It is formed after the compressed file is recognized in colab and successfully decompressed.

#### (4)	NotImplementedError: cannot convert symbolic tensor (2nd_target:0) to numpy array
####      During the last step of training, I was prompted with the above error again.
####      Solution: Add the following code at the beginning of the file:
####      pip install numpy==1.19.5
111111
####      Note: After adding this line of code, You must restart the runtime in order to use newly installed versions.
####      The problem occurs when upgrading numpy 1.19 to 1.20 and using RLlib from internally used. Just downgrade raytensorflow 2.2.
#### (5)  In order to speed up the training time, I changed the value of snapshot_count to 2.
####      If you have more than one GPU, the training speed can be quickly changed to 4, 6, etc.
## 4. Introduction to my dataset
#### I found 120 snail pictures on the Internet and processed them into a uniform square size of 128*128 with 1024 pixels. 
#### I try to generate my own dataset and train on StyleGan.
## 5. Display the final result
111111
#### Finally, the training was successfully carried out through multiple practices, and pictures were generated.

#### In fact, I prefer the half-finished product during the training process to the final training image. 
#### Their abstract outlines make me even more excited to create further. Each one has interesting textures.
#### I will be training on a larger number of image datasets in the future. This time, due to time constraints, 
#### I did not make further artistic creations, which is a pity for me.

## 7. Video link of my work:
https://youtu.be/dwVG4k0kG9M

## 8. the third-party resources were used in the creation of my project
#### Reference code link:
https://github.com/dvschultz/ml-art-colabs/blob/master/Stylegan2_ada_Custom_Training.ipynb

# In Conclusion
## In this file, I share the knowledge and reflections I gained while experimenting with stylegan2 in the Google colab server, 
## hoping to help others in their research and learning.

