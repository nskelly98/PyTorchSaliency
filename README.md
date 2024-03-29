# Repository: Saliency Map Generation using PyTorch

This repository contains code to generate saliency maps using PyTorch, leveraging information from two large, publicly available radiology datasets: the Society for Imaging Informatics in Medicine–American College of Radiology Pneumothorax Segmentation dataset and the Radiological Society of North America Pneumonia Detection Challenge dataset.

## Description

Saliency maps are invaluable tools in medical image analysis, aiding in the interpretation and understanding of deep learning models. This repository provides a comprehensive framework for generating saliency maps tailored to radiology datasets, with a focus on the following functionalities:

1. **Model Generation**:
   - **Folder 1: InceptionV3 and DenseNet121 Models**: Contains code for training and generating two different models, namely InceptionV3 and DenseNet121. These models are trained on the aforementioned radiology datasets, utilizing state-of-the-art techniques in deep learning for image segmentation and classification tasks.

2. **Saliency Map Techniques**:
   - **Folder 2: Gradient-based and Integrated Gradient Methods**: Includes implementations of various saliency map techniques such as Grad, Smooth Grad, Integrated Gradients, Smooth Integrated Gradients, and Guided backpropagation. These methods are implemented using the package specified in the PAIR/saliency repository, ensuring robustness and accuracy in saliency map generation.

3. **Class Activation Mapping (CAM) Techniques**:
   - **Folder 3: Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++**: Provides code for generating CAM-based saliency maps including Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++. These techniques are implemented using the TorchCAM package, which offers efficient and intuitive methods for visualizing model predictions and decision-making processes.

This repository serves as a comprehensive toolkit for researchers and practitioners in medical imaging, facilitating the interpretation and analysis of deep learning models trained on radiology datasets. By providing implementations of diverse saliency map techniques, it enables users to gain insights into model behavior and enhance the interpretability of medical image analysis systems.
