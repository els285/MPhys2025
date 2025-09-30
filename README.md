# MPhys2025
Common repository for 2025-26 MPhys work

<img width="256" height="256" alt="ChatGPT Image May 8, 2025, 11_34_51 AM" src="https://github.com/user-attachments/assets/942f64d8-1ecc-4cac-b0b0-519774627597" />
<img width="388" height="259" alt="image" src="https://github.com/user-attachments/assets/32754952-1f47-46d1-982c-2d35f5a92c61" />

# Google Drive Storage
We will store datasets on this Google Drive.
[Link to Google Drive](https://drive.google.com/drive/folders/1zteNmkQa9EV_ZfvHS91jHaT1o9bDR-_C?usp=sharing)

# Learning outcomes
* Proficiency in PyTorch (possibly extending to tools like PyTorch-Lightning)
* Proficiency in data analysis for particle physics with Scikit-HEP stack
* Building ML models for various HEP tasks
* Deploying large models on GPUs
* Possibly generating simulated datasets

# Possible research outcomes
* Test and benchmark different tools for classifying various specific processes
* Applying and extending these tools to multi-class classification
* Apply masked transformer idea for reconstructing arbitrary heavy resonance particle kinematics
* Comparing both of the above techniques to the HyPER tool
* Testing transformer regression for ttbar spin measurements [direct SDM elements, direct top kinematics]
* Adding in generative techniques for ttbar spin measurements

# Tutorials and documentation

### Slides on Intro2ML for Particle Physics [here](https://drive.google.com/file/d/17f46cMSA29RENtD4lB0MjeoLFmBOVhHA/view?usp=drive_link)
High-level overview (given to undergraduates); should give you the flavour of the field.

### Intro to ML 4 Physicists (by Ethan) [here](https://github.com/els285/Intro2NN4Physics/tree/main)
Covers:
  * Using the scikit-hep stack for HEP data analysis
  * Pedagogical introduction to classical ML with PyTorch
  * Building a DNN with PyTorch for signal/background classification

### PyTorch Tutorials
[PyTorch](https://docs.pytorch.org/tutorials/)

[PyTorch Lightning](https://lightning.ai/docs/pytorch/stable/starter/introduction.html)

### Manchester resources
[Manchester Computational Shared Facility](https://ri.itservices.manchester.ac.uk/csf3) - UoM computing infrastructure with access to GPUs
I will get you set up here in due course.

# Literature
### Introductions to Particle Physcs
* _Particles Physics_, Martin & Shaw
* _Introduction to Elementary Particle Physics_, Griffiths

### Machine Learning in HEP
[HEP ML Living Review](https://iml-wg.github.io/HEPML-LivingReview/)

### Reconstructing Kinematics of Top Quarks and Higgs Bosons
[HyPER paper](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.111.032004). Uses a graph neural network encoder and then a "hyperedge layer"
[SPANet - the HyPER competitor](https://www.nature.com/articles/s42005-024-01627-4). Uses a transformer encoder and tries to consider some physics symmetries.
[Nu2-Flows](https://journals.aps.org/prd/abstract/10.1103/PhysRevD.109.012005). Uses a transformer encoder and a normalising flow.

### Mask-Formers
[Original META MaskFormer paper](https://arxiv.org/abs/2107.06278)
[Latest example of MaskFormer in HEP](https://arxiv.org/abs/2508.20092). Uses the MaskFormer for effectively building the objects we see in the detector.

# Interesting code-bases
[MAncHEP-AI](https://github.com/els285/MancHEP-AI). A wrapper we have designed for models we train here in Manchester. A work in progress. Perhaps we can move our models here into this format down the line.
[SummerProject25 Transformer](https://github.com/youlin-meng/Particle_Transformer/tree/main)
[hep-attn](https://github.com/samvanstroud/hepattn/tree/main). An implementation of the MaskFormer for the above GLOW paper. We can hopefully use some of this.



# Working practices
This research will be computationally heavy, and we will do everything in Python. Recommend to be comfortable working in iPython notebooks (Jupyter Notebook, Google Colab, VSCode).
Recommend using VSCode or similar IDE for coding (VSCode is the best). Will also need access to a terminal (CLI). Good to learn to use GIT in due course.






  
