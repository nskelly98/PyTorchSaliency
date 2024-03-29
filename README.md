# Saliency Map Generation using PyTorch

This repository contains code to generate saliency maps using PyTorch, leveraging information from two large, publicly available radiology datasets: the Society for Imaging Informatics in Medicine–American College of Radiology Pneumothorax Segmentation dataset and the Radiological Society of North America Pneumonia Detection Challenge dataset. Each of the steps in generating ten different saliency maps are included in the folders provided. In the future, it would make more sense to implement more functions instead of replicating the code across each model and each dataset, but for now the included code is seperated this way.

## Description

Saliency maps are invaluable tools in medical image analysis, aiding in the interpretation and understanding of deep learning models. This repository provides a comprehensive framework for generating saliency maps tailored to radiology datasets, with a focus on the following functionalities:

1. **Model Generation**:
   - **Folder 1: InceptionV3 and DenseNet121 Models**: Contains code for training and generating two different models, namely InceptionV3 and DenseNet121. These models are trained on the aforementioned radiology datasets for classification tasks.

2. **Saliency Map Techniques**:
   - **Folder 2: Gradient-based and Integrated Gradient Methods**: Includes implementations of various saliency map techniques such as Grad, Smooth Grad, Integrated Gradients, Smooth Integrated Gradients, and Guided backpropagation. These methods are implemented using the package specified in the PAIR/saliency repository.

3. **Class Activation Mapping (CAM) Techniques**:
   - **Folder 3: Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++**: Provides code for generating CAM-based saliency maps including Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++. These techniques are implemented using the TorchCAM package.

.
