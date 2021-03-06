# SALAS (Satellite Auto-Labeling And Segmentation)
Supporting Github Repository for "Automated and Refined Application of Convolutional Neural Network Modeling to Metallic Powder Particle Satellite Detection" Article and based on 
the [AMPIS](https://github.com/rccohn/AMPIS) Framework.

This repository contains 3 sections: "sat_helpers", "data", and "demos"
 * The "sat_helpers" folder contains helper files of methods that are commonly used. This includes visualizing results, converting formats, exporting predictions, and more. 
 * The "data" folder contains all images of Scanning Electron Microscope micrographs included in the corresponding work under the folder "SEM". All images included are PNG format and held to a constant 1024x768 resolution to enable CNN trainings. In addition, the training and validation set annotations used for the final model can be found under the VIA folder. Here, the annotation software VGG Image Annotator (VIA) that was used used can also be found. Lastly, segmentations from the final prediction model on validation images are stored here and can be used to compare with the ground truth results to verify perforance. 
 * The "demos" folder contains examples for code to implement new features elaborated upon in the corresponding article as well as basic ones previously created. These features include, training a model, getting predictions from a trained model, converting predictions to annotations and exporting them, comparing image segmentations to ground truth data at a pixel level, quantifying performance imporvements over time by comparing multiple models performances at the same time, as well as interpretting calculated performance data into graphs that are easier to understand. 

NOTE: As it stands currently, the code and data used is in this repo are included and these files can be viewed to be determined what was done. However, the process of converting this into its own standalone framework to be installed is currently underway and as a result, these files do not currently run on their own. 
# Installation
The SALAS framework is dependent on a couple of packages including detectron2 before being installed. Detectron2 requires a Linux or Mac OS with Python 3.6 or higher. See INSTALLATION.md for a detailed desctription of requirements and step by step guide.

# Acknowledgements
This work is in part funder by the United States Army Research Laboratory under grant number W911NF-10-2-0098. This work used the Extreme Science and Engineering Discovery Enviroment (XSEDE), which is supported by Natational Science Foundation grant number DMR200035.
