# Enhancing Diabetic Retinopathy Detection with CNN-Based Models: A Comparative Study of UNET and Stacked UNET Architectures

This repository compares the performance of UNET and Stacked UNET architectures for diabetic retinopathy segmentation tasks using CNN-based models. The project is organized into separate experiment folders for single UNET vs stacked UNET and includes notebooks plus exported metrics.

## Repository Structure

- `Single_UNET/`  
  Notebook and metrics for the single UNET model.
- `Stacked_UNET/`  
  Notebook and metrics for the stacked UNET model.
- `Architectures/`  
  Architecture diagrams/images used in this README.
- `requirements.txt`  
  Python dependencies.
- `.gitignore`  
  Ignore rules for local data, outputs, checkpoints, etc. (you’ll add this)

## Dataset

This project uses the APTOS 2019 Blindness Detection dataset:

- [APTOS 2019 Blindness Detection (Kaggle)](https://www.kaggle.com/c/aptos2019-blindness-detection)

> Note: The dataset is not included in this repository. You must download it from Kaggle.

### Pre-processing
- Resize to `256x256`
- Convert to grayscale

### Dataset Setup (Recommended)

To avoid path issues, place data under a single shared directory at the repo root:

```text
Diabetic_Retinopathy-UNET_Stacked_UNET/
  data/
    APTOS/
      train.csv
      train_images/
        <image files>
```

> Notes:
> - The notebooks may contain hard-coded paths. Update them to point to the folders above.
> - If you prefer a different layout, keep it consistent and update notebook paths accordingly.
## Models Implemented

### UNET (Single)

Implements the traditional UNET architecture commonly used for medical image segmentation.

<p align="center">
  <img src="Architectures/UNET.png?raw=true" alt="UNET architecture" width="650" height="400">
</p>

### Stacked UNET

Implements a stacked-UNET approach intended to capture richer features and improve segmentation performance.

<p align="center">
  <img src="Architectures/UNET-2.png?raw=true" alt="Stacked UNET architecture" width="900" height="500">
</p>

## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/AmeyaUppina/Diabetic_Retinopathy-UNET_Stacked_UNET.git
   cd Diabetic_Retinopathy-UNET_Stacked_UNET
   ```

2. (Recommended) Create and activate a virtual environment:

   ```bash
   python -m venv .venv
   # Windows:
   .\.venv\Scripts\activate
   # macOS/Linux:
   source .venv/bin/activate
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

## Usage

Run the notebook corresponding to the model you want:

- Single UNET: `Single_UNET/Single_Stack_UNET.ipynb`
- Stacked UNET: `Stacked_UNET/2_Stacked_UNET.ipynb`

If a notebook fails due to missing files:
1. Search inside the notebook for dataset path variables/file paths (e.g., `train.csv`, `train_images`, or `data/`).
2. Update them to match your local dataset directory (see **Dataset Setup**).

## Tech Stack

<div align="center">

<img src="https://img.shields.io/badge/Python%20-%2314354C.svg?&style=for-the-badge&logo=python&logoColor=white" alt="Python" />
<img src="https://img.shields.io/badge/TensorFlow%20-%23FF6F00.svg?&style=for-the-badge&logo=tensorflow&logoColor=white" alt="TensorFlow" />
<img src="https://img.shields.io/badge/Keras%20-%23D00000.svg?&style=for-the-badge&logo=keras&logoColor=white" alt="Keras" />
<img src="https://img.shields.io/badge/OpenCV%20-%23white.svg?&style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV" />
<img src="https://img.shields.io/badge/NumPy%20-%23013243.svg?&style=for-the-badge&logo=numpy&logoColor=white" alt="NumPy" />

</div>

## Acknowledgements

- Thanks to Kaggle and the APTOS dataset providers.
- Thanks to the Keras/TensorFlow ecosystem for the deep learning framework.
- Thanks to the open-source community resources (e.g., Stack Overflow) for troubleshooting.
