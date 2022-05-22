# Thermal to RGB imaging project
ELEG 404 Digital Imaging Project at University of Delaware.

In this project, we are interested in training a convolutional autoencoder model to convert thermal images to RGB images. 

Initially, we acquired a wide range of images such as dogs, cars, tables, etc. However, this becomes a major challenge for the model to learn 
the relationship between thermal images and RGB images. So, we narrowed down images to only buildings on campus. Besides, there are 
some really dark RGB images, which make the model learn to output only black images. So we had to throw away these images. Interms of image colors,
we tried both colored thermal and RGB images, colored themal and gray RGB images, and both gray thermal and RGB images. The motivation to
consider grayscale images is that thermal color for a same object could be totally different if the object is in the shadow or under sunshine 
so that thermal color somehow interferes the learning of RGB objects. 

When it comes to the model structure, we used a three layer encoding and three layer
decoding model, we also adopted different loss functions including mean squered error (MSE) and structral similarity (SSIM) and we found that the SSIM leads to sharper output predicted RGB images than the same model using MSE as SSIM considered more structral information.

All data we acquired are in the data folder, the data we used for the final traininng are "Thermal Buildings" and "RGB Buildings". The two folders "Thermal" and "RGB" include all types of objects we initially acquired.

### Contributors to the project are: Jacob Stafford, Bright Lu, Steven Shreve, Fuli Wang



