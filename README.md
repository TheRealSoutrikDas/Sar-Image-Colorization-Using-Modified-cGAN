<p align="center"> <img src="https://github.com/user-attachments/assets/215a5f83-dacc-4ad8-8d50-bdf128c294e1" alt="SAR Colorization GAN Logo" width="500"/> </p> <h1 align="center">SAR Image Colorization Using a Modified Conditional GAN</h1> <p align="center"> <em>Enhancing SAR imagery using deep generative modeling with dual discriminators</em> </p> <p align="center"> <a href="https://github.com/your-username/Sar-Image-Colorization-Using-Modified-cGAN/actions"> <img src="https://img.shields.io/github/actions/workflow/status/your-username/Sar-Image-Colorization-Using-Modified-cGAN/python-app.yml?label=CI&logo=github&style=flat-square" alt="CI Status" /> </a> <img src="https://img.shields.io/badge/license-MIT-blue.svg?style=flat-square" alt="License" /> <img src="https://img.shields.io/badge/python-3.8%2B-green.svg?style=flat-square" alt="Python" /> <img src="https://img.shields.io/github/stars/your-username/Sar-Image-Colorization-Using-Modified-cGAN?style=social" alt="GitHub stars" /> </p>

# SAR Image Colorization Using a Modified Conditional GAN (cGAN)

This repository contains the implementation of a modified Conditional Generative Adversarial Network (cGAN) for the **colorization of Synthetic Aperture Radar (SAR) images**. The approach leverages a **dual-discriminator architecture** alongside a **U-Net-based generator** to enhance the realism and structural integrity of generated optical images from SAR inputs.

---

## 📘 Background

This work builds upon the paper:
**"A SAR-to-Optical Image Translation Method Based on Conditional Generative Adversarial Network (cGAN)"**
by *Li and Fu*
🔗 [Read the paper](https://www.semanticscholar.org/paper/A-SAR-to-Optical-Image-Translation-Method-Based-on-Li-Fu/3f99537a05196582f3f9f750d02b2995a8050b1f)

### Key Modifications:

* **Dual Discriminators**:

  * **Local Discriminator**: Captures fine-grained features from small patches of the image.
  * **Global Discriminator**: Assesses the overall realism of the entire image.
* **Generator Architecture**: Employs a **U-Net** to preserve spatial information via skip connections.
* The adversarial setup helps the network learn both local texture consistency and global image coherence.

---

## 🧠 Model Architecture

<p align="center"> <img src="https://github.com/user-attachments/assets/215a5f83-dacc-4ad8-8d50-bdf128c294e1" alt="Architecture" width="800"/> </p>
Figure: The modified cGAN architecture with a U-Net generator and dual discriminators.
---

## 🔍 Example Results

**Input SAR Image**
<table> <tr> <td align="center"><strong>Input SAR Image</strong></td> <td align="center"><strong>Colorized Output</strong></td> </tr> <tr> <td align="center"> <img src="https://github.com/user-attachments/assets/946e2747-3ed4-44f4-88a1-9b54bca9b3cb" alt="Input SAR" width="300"/> </td> <td align="center"> <img src="https://github.com/user-attachments/assets/dd3d1b35-f0bc-49e8-a267-b86d24c14bb1" alt="Output Colorized" width="300"/> </td> </tr> </table>
---

## ⚙️ Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Sar-Image-Colorization-Using-Modified-cGAN.git
cd Sar-Image-Colorization-Using-Modified-cGAN
```

### 2. Set Up Python Environment

Create and activate a virtual environment:

```bash
python -m venv venv
source venv/bin/activate  # or .\venv\Scripts\activate on Windows
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Download Pretrained Generator

Download the pretrained generator weights from Google Drive and place the file in the project root directory:
📥 [generator\_final.pth](https://drive.google.com/file/d/1AaIB38Ifc1uBNurf8huZJ0N7L1AWQ96M/view?usp=sharing)

### 5. Inference

1. Place SAR images to be colorized in the `output_images/` directory.
2. Run the generator script:

   ```bash
   python gen.py
   ```
3. Generated colorized images will be saved in the `input_images/` directory.

---

## 🗂 Directory Structure

```
├── gen.py                     # Inference script
├── generator_final.pth        # Pretrained model weights
├── requirements.txt           # Python dependencies
├── output_images/             # Folder for SAR input images
└── input_images/              # Output folder for generated colorized images
```

---

## 📝 Citation

If you find this project useful in your research or work, please consider citing the original paper:

> Li, Y., & Fu, K. (Year).
> *A SAR-to-Optical Image Translation Method Based on Conditional Generative Adversarial Network (cGAN)*
> [Semantic Scholar](https://www.semanticscholar.org/paper/A-SAR-to-Optical-Image-Translation-Method-Based-on-Li-Fu/3f99537a05196582f3f9f750d02b2995a8050b1f)

---

## 📄 License

This project is provided for **educational and research purposes only**. Please review the [LICENSE](LICENSE) file (if available) for more details.

---

## 🙏 Acknowledgments

* Inspired by advancements in SAR-to-optical translation and generative adversarial networks.
* Special thanks to the authors of the referenced paper for their foundational work.

---
