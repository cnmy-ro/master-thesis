# Predicting Tumor Hypoxia Map from FDG-PET/CT Images using GANs


Master's thesis project completed as part of my M.Sc. degree in Artificial Intelligence at Maastricht University, and in collaboration with [Maastro Clinical Data Science (CDS) imaging research group](https://github.com/Maastro-CDS-Imaging-Group).



----------------------
## Project Description
Tumor hypoxia is characterized by an insufficient oxygen concentration in certain localized regions of a tumor. Hypoxic cancer cells develop higher therapy resistance and greater migratory capability, thereby reducing the effectiveness of radiotherapy treatment. Positron Emission Tomography (PET) imaging has recently become a major focus of research for its use as an in vivo hypoxia detection tool. Hypoxia PET provides an oxygen concentration map that is overlaid on a Computed Tomography (CT) scan to enhance contrast around hypoxic regions, thereby enabling their localization. It can, therefore, be integrated into radiotherapy workflow to account for tumor hypoxia and adjust the radiation dosage accordingly. HX4-PET is an instance of hypoxia PET imaging that uses the newly developed radiotracer [18F]HX4. Despite its great potential in improving cancer treatment, HX4-PET imaging is expensive and is currently only limited to clinical trials. This work investigates a GAN-based computational alternative to hypoxia imaging. We apply image translation GANs to synthesize whole HX4-PET images from the more readily available FDG-PET and CT modalities, exploring both paired and unpaired translation approaches. Using the paired Pix2Pix as a reference method, unpaired translation with CycleGAN is studied and compared. We argue that naively applying the default CycleGAN system to our use case is a flawed strategy because the invertibility assumption of CycleGAN is seriously violated here, and propose a design modification to CycleGAN training for circumventing this issue and optimizing the system for our purpose. We perform an extensive evaluation of the GANs by first testing on a simulated translation task, followed by comprehensively evaluating on an appropriate 3D medical image dataset. We, additionally, perform a set of clinically relevant downstream tasks on the synthetic HX4-PET images to determine their clinical value. Our experiments show that the modified CycleGAN attains high image-level performance, close to that of Pix2Pix, and although our synthetic HX4-PET images may not yet meet the clinical standard, the results suggest that unpaired translation approaches could be more suitable for the task due to their immunity to noise induced in the training data by spatial misalignments.

- View the complete thesis [here](Master_Thesis-Chinmay_Rao.pdf).


-------
## Code

1. [ganslate](https://github.com/ganslate-team/ganslate): General-purpose GAN framework for image-to-image translation based on PyTorch, developed mainly by Ibrahim Hadzic ([@ibro45](https://github.com/ibro45)) and Suraj Pai ([@surajpaib](https://github.com/surajpaib)). In addition to having used heavily to drive my experiments, I contributed and still continue to contribute to this codebase.

2. [HX4-PET-translation](https://github.com/Maastro-CDS-Imaging-Group/HX4-PET-translation): Project-specific code -- Jupyter notebooks, scripts, and utility code for dataset preparation, data pre-processing, and output image evaluation.
