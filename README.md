# Advancing Object Detection: YOLOv4, Image Segmentation, and ConvNeXt - Reimplementation of the OneFormer model

## Features
- This version of OneFormer is an advanced neural network model designed for comprehensive image segmentation tasks, including semantic, instance, and panoptic segmentation. Building upon the original OneFormer architecture, this version integrates improvements in various components, offering more robust and accurate segmentation capabilities.
- I have used the OneFormer model from the paper "OneFormer: One Transformer to Rule Universal Image Segmentation" as a reference for re-implementations. I implemented my version of the OneFormer model from scratch and added more comments on each function. Which would be inside of newOneFormer.py (original code)
- Other code in this repository is copied from the OneFormer codebase. Here is the GitHub repository of the OneFormer model: https://github.com/SHI-Labs/OneFormer/tree/main

## Prerequisites
Before installing and using this reimplemented version of OneFormer, ensure you have the following prerequisites installed:

- Python 3.6 or higher
- PyTorch 1.7 or higher
- detectron2
- CUDA (if using GPU acceleration)

## Installation Instructions
- Clone the repository:
  - git clone [[URL to new OneFormer repository](https://github.com/jennychen1030/enhanced-one-former)]
  - cd newOneFormer
- Install required Python packages:
  - pip install -r requirements.txt

## Usage
- To use this version of OneFormer model, follow these steps:
  - Prepare Your Dataset: Ensure your dataset is in a format compatible with detectron2.
  - The dataset I used is ADE20K which can be obtained online: https://groups.csail.mit.edu/vision/datasets/ADE20K/
    - The ADE20K dataset, created by MIT and Adobe Research, is a comprehensive resource for semantic segmentation and scene parsing in computer vision. It features a diverse collection of indoor and outdoor images, each meticulously annotated at the pixel level. These annotations not only identify objects within each scene but also detail their parts and attributes.
      
  - Configuration: Adjust the configuration file (config.yaml) to suit your specific requirements, such as model parameters, training settings, etc.

  - Training the Model:
    - python train.py --config-file config.yaml
  - Inference:
    - For performing inference with a trained model, use:
      - python infer.py --config-file config.yaml --input [path to input image] --output [path for output]
  - Evaluation:
    - Evaluate the model's performance on a test dataset:
      - python evaluate.py --config-file config.yaml --test-data [path to test dataset]

## Customization
- You can customize the model for your specific needs by modifying the config.yaml file or altering the model's code, especially in areas like the panoptic_inference and instance_inference methods, to fine-tune its segmentation capabilities.

## Additional Notes
- This project is a reimplementation of the original OneFormer architecture and is intended for research and development purposes.
- For issues or feature requests, please file them on the GitHub issue tracker.

## Acknowledgement
- Thank the authors of OneFormer for releasing their helpful codebases.
