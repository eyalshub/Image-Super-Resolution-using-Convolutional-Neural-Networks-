# Image Super-Resolution using Convolutional Neural Networks 🖼️

This project focuses on improving the resolution of low-quality images using Convolutional Neural Networks (CNNs). The goal is to upscale images while preserving fine details, textures, and overall quality. Models were trained and tested using the **Pascal VOC 2007** dataset, and their performance is evaluated based on **Peak Signal-to-Noise Ratio (PSNR)**.

## 📂 Dataset Overview
- **Data Type:** Images (Low-resolution and High-resolution)
- **Dataset:** Pascal VOC 2007
- **Image Categories:** Various objects (e.g., person, dog, car, etc.)
- **Training Samples:** 5,000 low-resolution images and their corresponding high-resolution counterparts
- **Test Samples:** 1,000 images for evaluation

## 🛠️ Approach & Methodology
1. **Data Preparation:**  
   - **Preprocessing:** Images were downsampled to create low-resolution versions of the original high-resolution images.  
   - **Normalization:** Images were normalized to the range [0, 1] for better model convergence.

2. **Feature Engineering:**  
   - Extracted image features using Convolutional Layers  
   - Applied data augmentation techniques (rotation, flipping, scaling) to increase dataset diversity

3. **Modeling:**  
   - **Convolutional Neural Networks (CNN):**  
     - A simple CNN model for image super-resolution.  
   - **Enhanced Deep Super-Resolution Network (EDSR):**  
     - A deep model designed specifically for high-quality image upscaling.
   - **Residual Dense Network (RDN):**  
     - A network that focuses on capturing residual features for more accurate image reconstruction.
   - **VGG-based Model:**  
     - Used for perceptual loss based on pre-trained VGG network layers.

4. **Training Strategy:**  
   - Images were split into training and validation sets (80%/20%) for efficient model training.  
   - Optimized the model using **Adam optimizer** and **Mean Squared Error (MSE)** loss function.

## 📊 Results
| Model               | Resolution Factor | PSNR (dB) | Time to Train | Epochs |
|---------------------|-------------------|-----------|---------------|--------|
| CNN (Basic)         | 2x                | 24.2      | 5 hours       | 50     |
| EDSR                | 4x                | 29.5      | 12 hours      | 100    |
| RDN                 | 2x                | 28.0      | 8 hours       | 80     |
| VGG-based Model     | 2x                | 27.8      | 6 hours       | 60     |

## 🚀 Key Takeaways
- **Best Model:** **EDSR** achieved the highest PSNR of **29.5 dB** when upscaling images by 4x.  
- **Challenges:**  
  - High computational cost for training deep models  
  - Dealing with artifacts in upscaled images  
- **Solutions Applied:**  
  - Used deep residual networks to enhance image reconstruction  
  - Applied perceptual loss with VGG for better quality in terms of texture and detail

## 🔍 Future Improvements
- Explore the use of **Generative Adversarial Networks (GANs)** for higher-quality upscaling  
- Experiment with different image datasets and image formats  
- Fine-tune hyperparameters and train models with more data for better performance

## 📝 Authors
- Eyal Shubeli 


