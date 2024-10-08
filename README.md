# Sar-Image-Colorization-Using-Modified-cGAN
Colorization of SAR images using a modified conditional GAN which is using dual discriminator one for local characteristics other for the global.
This is based on the research paper A SAR-to-Optical Image Translation Method Based on Conditional Generation Adversarial Network (cGAN)
link to that research paper: https://www.semanticscholar.org/paper/A-SAR-to-Optical-Image-Translation-Method-Based-on-Li-Fu/3f99537a05196582f3f9f750d02b2995a8050b1f
the discriminator in this research paper has been further modified such that it looks for smaller details in smaller patches and also using a global discriminator to discriminate the image globally.
also using a UNET fir the generator. This is over all an adverserial model.
![2-Figure1-1](https://github.com/user-attachments/assets/215a5f83-dacc-4ad8-8d50-bdf128c294e1)

Input image:

![ROIs1868_summer_s1_59_p16](https://github.com/user-attachments/assets/946e2747-3ed4-44f4-88a1-9b54bca9b3cb)
    
Output image:

![generated_ROIs1868_summer_s1_59_p16](https://github.com/user-attachments/assets/dd3d1b35-f0bc-49e8-a267-b86d24c14bb1)

Setup:
1. create a python virtual environment
2. activate the environment
3. install all dependencies using requirements.txt
4. download and paste the generator_final.pth file to the project directory. link: https://drive.google.com/file/d/1AaIB38Ifc1uBNurf8huZJ0N7L1AWQ96M/view?usp=sharing
5. paste sar images to be colorized to output_images folder.
6. run the gen python script.

The generated images shoud appear in input_images.

Thank you.
