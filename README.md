# Text_to_image_generation_with_Dreambooth
This project transforms textual descriptions into high-quality images & involves using machine learning models and neural networks to generate professional attire images from regular images of women. It employs the `runwayml/stable-diffusion-v1-5` model and fine-tunes it using Dreambooth on the established dataset of 1000 images. The project leverages numerous tools and frameworks including Transformers, PyTorch, and Hugging Face’s diffusers.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Model Training](#model-training)
- [Data Preparation](#data-preparation)
- [Results](#results)
- [Contributing](#contributing)
- [Contact](#contact)

## Prerequisites
Before you begin, ensure you have met the following requirements:
- Python 3.10 or higher installed on your machine
- Access to Google Colab (recommended for GPU support)
- A connected and configured Google Drive to access datasets

## Installation

1. Clone the repository:
```bash
git clone https://github.com/anou1234/Text_to_image_generation_with_Dreambooth.git
```

2.Navigate to the project directory:
```bash
cd myproject
```
3. Install the required dependencies:
```bash

pip install transformers torch bertviz datasets
git clone https://github.com/ShivamShrirao/diffusers
cd diffusers/
pip install -e .
pip install bitsandbytes
cd ../
pip install -r requirements.txt
```
### Usage

1. Upload your image dataset. Uploading by mounting Google Drive is recommended. Adjust paths as appropriate:
```bash

import os
import shutil
from google.colab import drive
drive.mount('/content/drive')
source_dir = "/content/drive/MyDrive/woman" #dataset folder
destination_dir = "/content/images"
num_files_to_copy = 100
```
Fine-tune the model using provided scripts in the examples/dreambooth directory.

### Model Training

#### Training a customized model involves the following steps:

- Setting up an accelerated environment for efficient computation.
- Using the notebook gen_ai_dreambooth.ipynb and following instructions to run the cell blocks for model training and fine-tuning.
  
### Data Preparation

Prepare your data as follows:

- Ensure images are stored correctly in your dataset folder. Eg. For a ```'woman'``` token dataset, the images should be named as ```"woman_1"``` , ```"woman_2"``` , and so on.
- Modify file paths as required in scripts to point to directories storing your data.

### Results

Once the model is trained, generate and visualize your results. Evaluate the model's effectiveness in transforming images and enhancing attributes specified during training.

### Contributing
Contributions are always welcome! Please fork the repository and create a pull request. For major changes, please open an issue first to discuss what you would like to change.

### Contact

- **Author**: Anoushka Srivastava
- **Email**: anoushkathegreat28@gmail.com/anoushka.srivastava.21cse@bmu.edu.in
- **GitHub**: [anou1234](https://github.com/anou1234)
