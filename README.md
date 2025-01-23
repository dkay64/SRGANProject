# SRGAN Project

A **Super-Resolution Generative Adversarial Network (SRGAN)** designed to upscale low-resolution images into high-resolution ones. This project is inspired by the paper [*Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network*](https://arxiv.org/pdf/1609.04802.pdf).  

## Features
- Converts low-resolution images (32x32) into high-resolution images (128x128) using a GAN-based approach.
- Trained on a subset of the **MIRFLICKR-25K dataset** with preprocessed data for effective training.  

---

## Dataset

- **Source**: [MIRFLICKR-25K dataset](https://press.liacs.nl/mirflickr/mirdownload.html)  
  This dataset contains 25,000 images that are free to use for academic purposes.  

- **Preprocessing**:  
  Images were resized into two sets:  
  - **High Resolution (HR):** 128x128  
  - **Low Resolution (LR):** 32x32  
  Preprocessing was done using the script `DK_SRGANProj_prepare_dataset.py`.  

---

## Model Training

- **Training Details**:
  - Model file: `gen_e_10.h5`  
  - Training Data: A subset of 5,000 images from the dataset  
  - Training Duration: 10 epochs  
  - Training Script: `DK_SRGANProj_training.py`  
  - Hardware: Local machine with an **RTX 4070 GPU**

---

## Potential Extensions

### Cloud Training for Enhanced Performance
- **Problem**: Training on a local machine limits the number of images and epochs due to hardware and time constraints.  
- **Proposed Solution**: Migrate training to a remote cloud server to:  
  - Train on the entire dataset (25,000 images).  
  - Increase the number of epochs to 100,000 for improved accuracy and robustness.  

### Suggested Platforms
- [AWS EC2](https://aws.amazon.com/ec2/)  
- [Microsoft Azure](https://azure.microsoft.com/en-us/)  
- [Google Cloud Platform (GCP)](https://cloud.google.com/)  

---

## How to Use

1. **Dataset Preparation**:  
   Use `DK_SRGANProj_prepare_dataset.py` to resize the original images into high and low resolution.  

2. **Training**:  
   Run `DK_SRGANProj_training.py` to train the GAN model.  

3. **Model Inference**:  
   Use the trained model (`gen_e_10.h5`) to upscale low-resolution images.  

---

## Future Research Directions

- Exploring alternative GAN architectures for better performance (e.g., ESRGAN, BigGAN).  
- Implementing distributed training across multiple GPUs for scalability.  
- Investigating the use of synthetic datasets to supplement training data.  
- Evaluating model performance using metrics like PSNR and SSIM.  

---

## References

- Paper: [*Photo-Realistic Single Image Super-Resolution Using a Generative Adversarial Network*](https://arxiv.org/pdf/1609.04802.pdf)  
- Dataset: [MIRFLICKR-25K dataset](https://press.liacs.nl/mirflickr/mirdownload.html)  

---

**Author**: Dhruv Kesavarap  
