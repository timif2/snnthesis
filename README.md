# Adversarial Robustness of Rate - Encoded Spiking Neural Networks

## Description

This repository hosts the code and the thesis for my Masters project, for the degree of Master in Statistics.

## Installation and Requirements

This project requires the following Python packages:

- eagerpy==0.30.0
- foolbox==3.3.4
- snnTorch==0.9.1
- spikingjelly==0.0.0.0.14
- torch==2.4.0
- torchattacks==3.5.1
- torchvision==0.19.0
- tqdm==4.66.4

## Installation

To install the required packages, you can use the `requirements.txt` file. Run the following command in your
project directory:

```
pip install -r requirements.txt
```

## Targeted and non - targeted attacks

- Non-targeted attacks: All attacks run in this way do not shift the labels of the original data in such a way to form any targeted attack.
- Targeted attacks: All attacks run in this way shift the labels of the original data by one.

When running either notebook (targeted or non-targeted), this code produces an application in an external window opens which gives the user the ability to set different parameters:

- Select model: Model choice. Choose between QIF, LIF and Izhikevich model for analysis (default: QIF)
- Select attack: Black or white box adversarial attack. Choose between PGD, FGSM and Pixle attack (default: PGD)
- Select epsilon: Attack Intensity. Options: 8/255, 16/255, 32/255, 64/255 (default: 8/255)
- Select timesteps: Model training timesteps. type: int (default: 15)
- (If attack == Pixle) Size of patch: Size of attack patch 10%,20%,..,100% (default: 10%). Note that if
- attack != Pixle and size of patch != 0.1 an error will stop the app from running.
