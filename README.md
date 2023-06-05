# Video Prediction on Moving MNIST 
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1t03e6xtX_JCjevhsut-pJAShWj7omdy-/view?usp=drive_link)
## Project description
This repository contains the group's project for the Deep Learning Course in La Sapienza University of Rome, held by Professor Fabrizio Silvestri.  
We benchmarked 4 different architectures on the Moving MNIST dataset, . These were respectively  
    1. Vanilla Encoder-Decoder;  
    2. [SimVP](https://arxiv.org/abs/2206.05099)  
    3. [Temporal Attention Unit](https://arxiv.org/abs/2206.12126)  
    4. [SimVP2](https://arxiv.org/abs/2211.12509) 

The domain of interest is SpatioTemporal Predictive learning, these take as input frames of moving digits, and aim to predict their future frames.  
We have been able to replicate the experiments, and in this repo is available the code. Due to missing information there are some issues with the Temporal Attention Unit reproducibility.  

## How to use this repository  
After having cloned the repository, make sure that a 'models.zip' file is included in the folder. This contains the pretrained models, that can be tested immediately in one of the notebooks. The file is downloadable at this [link](https://drive.google.com/file/d/1DlcSa3EjgF9d4ugH-rA6pEEmwP7K-4Ot/view?usp=drive_link). The file will be unzipped within the notebook. In 'VP_on_MMNIST.ipynb', is possible to train new and past models. In colab is also possible to test the models.  
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://drive.google.com/file/d/1t03e6xtX_JCjevhsut-pJAShWj7omdy-/view?usp=drive_link).  
*WARNING*: Colab and github versions are slightly different, so make sure to open the one that you desire.  
## Project Organization  
Once you have run the notebook, the organization of this repo. should be like this:  
* data/ :  (Automatically downloaded in the notebook)
    * processed/ : Train data from external repository, downloaded inplace
    * raw/ : Test data from external repository, downloaded inplace (only 1000 samples) 
* MovingMNIST/ :(Automatically downloaded in the notebook) External repository used to download train & test data of Moving MNIST  
* models/ : (models.zip unzipped in the notebook, or manually if preferred)  
    * random_model.pt : Vanilla Encoder-Decoder pre-trained model
    * simvp_model.pt : SimVP pre-trained model
    * simvp2100.pt : SimVP2 pre-trained model (for 100 epochs, state-of-the-art)  
* mnist_test_seq.npy : (Automatically downloaded in the notebook) test data (10000 samples)  
* models.zip : (Downloaded manually from this [link](https://drive.google.com/file/d/1DlcSa3EjgF9d4ugH-rA6pEEmwP7K-4Ot/view?usp=drive_link))  
* presentation.pptx : PowerPoint presentation with brief summary of our work.  
* report.pdf : Detailed description of our experiments, and theoretical description of our approach.  
* VP_on_MMNIST.ipynb : Code for train and experiments reproducibility, in the colab version above is also possible to conduct more experimental validations  

### Project Contributors
* Mattia Castelmare - 1815675
* Andrea Giuseppe Di Francesco - 1836928
* Enrico Fazzi - 2003876
