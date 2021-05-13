# Machine Learning For Tagging Graphic Designs


## Table of contents
  - [Project Description](#project-description)
  - [Getting Started](#getting-started)
  - [Usage](#usage)
  - [Additional Resources](#-additional-resources)


## Project Description

In this project we train and deploy a machine learning model to automatically predict the tags associated with a given image. 

Please read the [project overview](PROJECT.md) before continuing. It contains detailed information about: the purpose of our project, the creation of our dataset, the tools we used to accomplish the goal and more.

## Getting Started
  Follow the [set-up instructions](SETUP.md). After completing these steps you should have the following:
  1. An AWS account
  2. An S3 Bucket named *multi-label-data* with the following structure:
      
          multi-label-data/
            training/
              train.rec
            validation/
              val.rec
            output/
  3. A notebook instance in sagemaker with three files called train tune and deploy.

## Usage

Now that you have everything in place you are ready to train, tune and deploy the model.

Open the sagemaker notebook instance you created to begin.

### Training

To train a model with a fixed set of hyper-parameters open the file train.ipynb in the notebook instance and follow the instructions.

### Tuning

To utilize sagemakers hyper-parameter tuning feature and train multiple models with ranges of hyper-parameters in order to find the best ones open tune.ipynb in the notebook instance and follow the instructions.

### Deploying

To deploy a trained model to an endpoint open deploy.ipynb in the notebook instance and follow the instructions.

## Additional Resources


