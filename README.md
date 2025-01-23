# SRGANProject

A GAN to convert low resolution images into high resolution, this SR GAN project is inspired by the following paper:
https://arxiv.org/pdf/1609.04802.pdf

Dataset used:
https://press.liacs.nl/mirflickr/mirdownload.html
This website includes  a dataset (mirflickr25k.zip) which contains 25,000 images, which I then resized into high resolution (128x128) and low resolution (32x32) using the script in DK_SRGANProj_prepare_dataset.py.

The model (in gen_e_10.h5) is currently trained on 5000 of the images (10 epochs).

Potential option for extension/area of research: how to train on remote cloud server (i.e. AWS, Azure, etc.) instead of on the local machine (RTX 4070) to have faster training.
