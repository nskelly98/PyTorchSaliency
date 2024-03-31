# Saliency Map Generation using PyTorch

This repository contains code to generate saliency maps using PyTorch, leveraging information from two large, publicly available radiology datasets: the Society for Imaging Informatics in Medicine–American College of Radiology Pneumothorax Segmentation dataset and the Radiological Society of North America Pneumonia Detection Challenge dataset. Each of the steps in generating ten different saliency maps are included in the folders provided. This code is based on recreating previous research by Arun and Gaw, "Assessing the Trustworthiness of Saliency Maps for Localizing Abnormalities in Medical Imaging" [1] in PyTorch rather than TensorFlow. In the future, it would make more sense to implement more functions instead of replicating the code across each model and each dataset, but for now the included code is seperated this way.

## Description

Saliency maps are invaluable tools in medical image analysis, aiding in the interpretation and understanding of deep learning models. This repository provides a comprehensive framework for generating saliency maps tailored to radiology datasets, with a focus on the following functionalities:

1. **Model Generation**:
   - **Folder 1: InceptionV3 and DenseNet121 Models**: Contains code for training and generating two different models, namely InceptionV3 and DenseNet121. These models are trained on the aforementioned radiology datasets for classification tasks.

2. **Saliency Map Techniques**:
   - **Folder 2: Gradient-based and Integrated Gradient Methods**: Includes implementations of various saliency map techniques such as Grad, Smooth Grad, Integrated Gradients, Smooth Integrated Gradients, and Guided backpropagation. These methods are implemented using the package specified in the PAIR/saliency repository.

3. **Class Activation Mapping (CAM) Techniques**:
   - **Folder 3: Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++**: Provides code for generating CAM-based saliency maps including Grad-CAM, Guided Grad-CAM, ScoreCAM, and GradCAM++. These techniques are implemented using the TorchCAM package.

4. **Localization Utility**:
   - **Folder 4: Utility Measurement**: Includes the code for measuring the localization utility of each map in AUPRC. Each notebook represents each of the datasets, comparing them to their ground-truth masks.
  
5. **Sensitivity to Model Weight Randomization**:
   - **Folder 5: Sensitivity Measurement**: The code generated for randomizing the model weights for the InceptionV3 Model. From there, generate 50 saliency maps were produced from the previous code in Saliency Map techniques. Finally, the SSIM of each of the pairs of maps are compared and calculated.
  
The Inter-Architecture repeatability and Intra-Architecture reproducibility measurements are generated from initializing the models in folder one differently and reproducing the maps for the new models. Afterwards, the SSIM is compared using the same code in Sensitivity Measurement. 

1. Nishanth Arun, Nathan Gaw, Praveer Singh, Ken Chang, Mehak Aggarwal,
Bryan Chen, Katharina Hoebel, Sharut Gupta, Jay Patel, Mishka Gidwani,
Julius Adebayo, Matthew D. Li, and Jayashree Kalpathy-Cramer. Assessing
the (un)trustworthiness of saliency maps for localizing abnormalities in medical
imaging, 2021.
